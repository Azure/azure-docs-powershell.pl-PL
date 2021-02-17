---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178778"
---
# <span data-ttu-id="ef9a5-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="ef9a5-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="ef9a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9a5-103">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="ef9a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef9a5-104">SYNTAX</span></span>

### <span data-ttu-id="ef9a5-105">ObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ef9a5-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef9a5-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef9a5-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef9a5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef9a5-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef9a5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef9a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ef9a5-109">Usuwa grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="ef9a5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef9a5-110">EXAMPLES</span></span>

### <span data-ttu-id="ef9a5-111">Przykład 1. Usuwanie grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="ef9a5-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ef9a5-112">Usuwa grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="ef9a5-113">Przykład 2. Usuwanie grupy za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="ef9a5-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="ef9a5-114">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i potoki, które Remove-AzADGroup usunąć grupę z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="ef9a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef9a5-115">PARAMETERS</span></span>

### <span data-ttu-id="ef9a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9a5-116">-DefaultProfile</span></span>
<span data-ttu-id="ef9a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a5-118">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="ef9a5-118">-DisplayName</span></span>
<span data-ttu-id="ef9a5-119">Nazwa wyświetlana grupy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="ef9a5-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ef9a5-120">-Force</span></span>
<span data-ttu-id="ef9a5-121">Jeśli jest określona, nie należy prosić o potwierdzenie usunięcia grupy.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef9a5-122">-InputObject</span></span>
<span data-ttu-id="ef9a5-123">Object representation of the group to be removed.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a5-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ef9a5-124">-ObjectId</span></span>
<span data-ttu-id="ef9a5-125">Identyfikator obiektu grupy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef9a5-126">-PassThru</span></span>
<span data-ttu-id="ef9a5-127">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef9a5-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef9a5-128">-Confirm</span></span>
<span data-ttu-id="ef9a5-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef9a5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef9a5-130">-WhatIf</span></span>
<span data-ttu-id="ef9a5-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef9a5-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef9a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9a5-133">CommonParameters</span></span>
<span data-ttu-id="ef9a5-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9a5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef9a5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9a5-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef9a5-136">INPUTS</span></span>

### <span data-ttu-id="ef9a5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ef9a5-137">System.String</span></span>

### <span data-ttu-id="ef9a5-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ef9a5-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ef9a5-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef9a5-139">OUTPUTS</span></span>

### <span data-ttu-id="ef9a5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef9a5-140">System.Boolean</span></span>

## <span data-ttu-id="ef9a5-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef9a5-141">NOTES</span></span>

## <span data-ttu-id="ef9a5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef9a5-142">RELATED LINKS</span></span>