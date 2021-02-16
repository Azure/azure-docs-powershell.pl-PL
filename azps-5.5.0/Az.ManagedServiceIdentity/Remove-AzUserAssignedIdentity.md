---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187498"
---
# <span data-ttu-id="79782-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="79782-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="79782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79782-102">SYNOPSIS</span></span>
<span data-ttu-id="79782-103">Usuwa tożsamość przypisaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79782-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="79782-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79782-104">SYNTAX</span></span>

### <span data-ttu-id="79782-105">ResourceGroupAndNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="79782-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79782-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79782-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79782-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79782-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79782-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="79782-108">DESCRIPTION</span></span>
<span data-ttu-id="79782-109">Wartość **Remove-AzUserAssignedIdentity** usuwa określoną tożsamość przypisaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79782-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="79782-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79782-110">EXAMPLES</span></span>

### <span data-ttu-id="79782-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79782-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="79782-112">W tym przykładzie polecenie cmdlet usuwa identyfikator **tożsamości 1** w grupie zasobów **PSRG.**</span><span class="sxs-lookup"><span data-stu-id="79782-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="79782-113">True (Prawda)</span><span class="sxs-lookup"><span data-stu-id="79782-113">True</span></span>

## <span data-ttu-id="79782-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79782-114">PARAMETERS</span></span>

### <span data-ttu-id="79782-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="79782-115">-AsJob</span></span>
<span data-ttu-id="79782-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79782-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79782-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79782-117">-DefaultProfile</span></span>
<span data-ttu-id="79782-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79782-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79782-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="79782-119">-Force</span></span>
<span data-ttu-id="79782-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="79782-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="79782-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79782-121">-InputObject</span></span>
<span data-ttu-id="79782-122">Obiekt Identity.</span><span class="sxs-lookup"><span data-stu-id="79782-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79782-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79782-123">-Name</span></span>
<span data-ttu-id="79782-124">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="79782-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79782-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79782-125">-ResourceGroupName</span></span>
<span data-ttu-id="79782-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79782-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79782-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79782-127">-ResourceId</span></span>
<span data-ttu-id="79782-128">Identyfikator zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="79782-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79782-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79782-129">-Confirm</span></span>
<span data-ttu-id="79782-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79782-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79782-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79782-131">-WhatIf</span></span>
<span data-ttu-id="79782-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79782-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79782-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79782-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79782-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79782-134">CommonParameters</span></span>
<span data-ttu-id="79782-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79782-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79782-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79782-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79782-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79782-137">INPUTS</span></span>

### <span data-ttu-id="79782-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="79782-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="79782-139">System.String</span><span class="sxs-lookup"><span data-stu-id="79782-139">System.String</span></span>

## <span data-ttu-id="79782-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79782-140">OUTPUTS</span></span>

### <span data-ttu-id="79782-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79782-141">System.Boolean</span></span>

## <span data-ttu-id="79782-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79782-142">NOTES</span></span>

## <span data-ttu-id="79782-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79782-143">RELATED LINKS</span></span>
