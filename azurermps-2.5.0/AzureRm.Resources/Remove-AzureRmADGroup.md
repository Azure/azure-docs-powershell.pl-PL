---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 511d028c8307e53884cfa16472021fc59760b929
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897241"
---
# <span data-ttu-id="fd468-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="fd468-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="fd468-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd468-102">SYNOPSIS</span></span>
<span data-ttu-id="fd468-103">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd468-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd468-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd468-104">SYNTAX</span></span>

### <span data-ttu-id="fd468-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd468-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd468-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd468-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd468-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd468-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd468-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fd468-108">DESCRIPTION</span></span>
<span data-ttu-id="fd468-109">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd468-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="fd468-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd468-110">EXAMPLES</span></span>

### <span data-ttu-id="fd468-111">Przykład 1 — Usuwanie grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="fd468-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="fd468-112">Usuwa grupę z identyfikatorem obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fd468-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="fd468-113">Przykład 2 — Usuwanie grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="fd468-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="fd468-114">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i potokach, do których Remove-AzureRmADGroup usunąć grupę z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fd468-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="fd468-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd468-115">PARAMETERS</span></span>

### <span data-ttu-id="fd468-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd468-116">-DefaultProfile</span></span>
<span data-ttu-id="fd468-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd468-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd468-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fd468-118">-DisplayName</span></span>
<span data-ttu-id="fd468-119">Nazwa wyświetlana grupy, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="fd468-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="fd468-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fd468-120">-Force</span></span>
<span data-ttu-id="fd468-121">Jeśli ta argument jest określona, nie prosi o potwierdzenie usunięcia grupy.</span><span class="sxs-lookup"><span data-stu-id="fd468-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="fd468-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fd468-122">-InputObject</span></span>
<span data-ttu-id="fd468-123">Reprezentacja obiektu grupy, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="fd468-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="fd468-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fd468-124">-ObjectId</span></span>
<span data-ttu-id="fd468-125">Identyfikator obiektu grupy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fd468-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="fd468-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd468-126">-PassThru</span></span>
<span data-ttu-id="fd468-127">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="fd468-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fd468-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd468-128">-Confirm</span></span>
<span data-ttu-id="fd468-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd468-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd468-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd468-130">-WhatIf</span></span>
<span data-ttu-id="fd468-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd468-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd468-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd468-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd468-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd468-133">CommonParameters</span></span>
<span data-ttu-id="fd468-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd468-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd468-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd468-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd468-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd468-136">INPUTS</span></span>

### <span data-ttu-id="fd468-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fd468-137">System.Guid</span></span>

### <span data-ttu-id="fd468-138">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="fd468-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="fd468-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd468-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fd468-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd468-140">OUTPUTS</span></span>

### <span data-ttu-id="fd468-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd468-141">System.Boolean</span></span>

## <span data-ttu-id="fd468-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd468-142">NOTES</span></span>

## <span data-ttu-id="fd468-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd468-143">RELATED LINKS</span></span>
