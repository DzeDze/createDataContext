# createDataContext
A helper that provide Context and Provider to pass state through child components

# HOW TO USE

# For each data context:

- import createDataContext
- create a reducer:

const reducer(state, action) => {
	//implement execution code for each action type
}

const action1 = dispatch=> {
	return ()=> {
		dispatch({type: type, payload: payload});
	}
}

const action2 = dispatch=> {
	return (something)=> {
		dispatch({type: type, payload: something});
	}
}

export const {Context , Provider} = createDataContext(
    reducer,
    { action1, action2},
    initialState // could be anything like ‘’, [], 0, etc.
);

# Wrap children that you want to use the context between <Provider>:

<Provider>
 	<ChildComponent>
</Provider>
