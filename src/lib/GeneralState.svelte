<script>
    let s = {}

    const f = {
        upgradeLvl0: (field, value) => {
            s = {
                ...s,
                [field]: value
            }
        },
        upgradeLvl1: (l1, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [field]: value
                }
            }
        },
        upgradeLvl2: (l1, l2, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [field]: value
                    }
                }
            }
        },
        upgradeLvl3: (l1, l2, l3, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [l3]: {
                            ...s?.[l1]?.[l2]?.[l3] || {},
                            [field]: value
                        }
                    }
                }
            }
        },
        upgradeLvl4: (l1, l2, l3, l4, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [l3]: {
                            ...s?.[l1]?.[l2]?.[l3] || {},
                            [l4]: {
                                ...s?.[l1]?.[l2]?.[l3]?.[l4] || {},
                                [field]: value
                            }
                        }
                    }
                }
            }
        },
        upgradeLvl5: (l1, l2, l3, l4, l5, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [l3]: {
                            ...s?.[l1]?.[l2]?.[l3] || {},
                            [l4]: {
                                ...s?.[l1]?.[l2]?.[l3]?.[l4] || {},
                                [l5]: {
                                    ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5] || {},
                                    [field]: value
                                }
                            }
                        }
                    }
                }
            }
        },
        upgradeLvl6: (l1, l2, l3, l4, l5, l6, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [l3]: {
                            ...s?.[l1]?.[l2]?.[l3] || {},
                            [l4]: {
                                ...s?.[l1]?.[l2]?.[l3]?.[l4] || {},
                                [l5]: {
                                    ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5] || {},
                                    [l6]: {
                                        ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5]?.[l6] || {},
                                        [field]: value
                                    }
                                }
                            }
                        }
                    }
                }
            }
        },
        upgradeLvl7: (l1, l2, l3, l4, l5, l6, l7, field, value) => {
            s = {
                ...s,
                [l1]: {
                    ...s?.[l1] || {},
                    [l2]: {
                        ...s?.[l1]?.[l2] || {},
                        [l3]: {
                            ...s?.[l1]?.[l2]?.[l3] || {},
                            [l4]: {
                                ...s?.[l1]?.[l2]?.[l3]?.[l4] || {},
                                [l5]: {
                                    ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5] || {},
                                    [l6]: {
                                        ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5]?.[l6] || {},
                                        [l7]: {
                                            ...s?.[l1]?.[l2]?.[l3]?.[l4]?.[l5]?.[l6]?.[l7] || {},
                                            [field]: value
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
            }
        },
    }

    export { s, f }
</script>