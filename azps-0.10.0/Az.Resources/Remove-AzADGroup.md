---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892457"
---
# <span data-ttu-id="b0a51-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b0a51-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="b0a51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a51-103">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0a51-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="b0a51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0a51-104">SYNTAX</span></span>

### <span data-ttu-id="b0a51-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0a51-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a51-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a51-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a51-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a51-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a51-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0a51-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a51-109">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0a51-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="b0a51-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0a51-110">EXAMPLES</span></span>

### <span data-ttu-id="b0a51-111">Przykład 1 — Usuwanie grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="b0a51-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b0a51-112">Usuwa grupę z identyfikatorem obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b0a51-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="b0a51-113">Przykład 2 — Usuwanie grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="b0a51-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="b0a51-114">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i potokach, do których Remove-AzADGroup usunąć grupę z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b0a51-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="b0a51-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0a51-115">PARAMETERS</span></span>

### <span data-ttu-id="b0a51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a51-116">-DefaultProfile</span></span>
<span data-ttu-id="b0a51-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b0a51-118">-DisplayName</span></span>
<span data-ttu-id="b0a51-119">Nazwa wyświetlana grupy, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="b0a51-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b0a51-120">-Force</span></span>
<span data-ttu-id="b0a51-121">Jeśli ta argument jest określona, nie prosi o potwierdzenie usunięcia grupy.</span><span class="sxs-lookup"><span data-stu-id="b0a51-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0a51-122">-InputObject</span></span>
<span data-ttu-id="b0a51-123">Reprezentacja obiektu grupy, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="b0a51-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b0a51-124">-ObjectId</span></span>
<span data-ttu-id="b0a51-125">Identyfikator obiektu grupy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b0a51-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0a51-126">-PassThru</span></span>
<span data-ttu-id="b0a51-127">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="b0a51-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0a51-128">-Confirm</span></span>
<span data-ttu-id="b0a51-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a51-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a51-130">-WhatIf</span></span>
<span data-ttu-id="b0a51-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a51-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0a51-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a51-133">CommonParameters</span></span>
<span data-ttu-id="b0a51-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a51-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a51-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a51-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0a51-136">INPUTS</span></span>

### <span data-ttu-id="b0a51-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b0a51-137">System.Guid</span></span>

### <span data-ttu-id="b0a51-138">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b0a51-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="b0a51-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0a51-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b0a51-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0a51-140">OUTPUTS</span></span>

### <span data-ttu-id="b0a51-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0a51-141">System.Boolean</span></span>

## <span data-ttu-id="b0a51-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0a51-142">NOTES</span></span>

## <span data-ttu-id="b0a51-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0a51-143">RELATED LINKS</span></span>
