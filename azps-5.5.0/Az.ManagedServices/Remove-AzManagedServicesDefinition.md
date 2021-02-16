---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187459"
---
# <span data-ttu-id="4cabd-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4cabd-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4cabd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cabd-102">SYNOPSIS</span></span>
<span data-ttu-id="4cabd-103">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cabd-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="4cabd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cabd-104">SYNTAX</span></span>

### <span data-ttu-id="4cabd-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4cabd-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cabd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cabd-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cabd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cabd-107">DESCRIPTION</span></span>
<span data-ttu-id="4cabd-108">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cabd-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="4cabd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cabd-109">EXAMPLES</span></span>

### <span data-ttu-id="4cabd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4cabd-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="4cabd-111">Usuwa definicję rejestracji według nazwy w zakresie domyślnym.</span><span class="sxs-lookup"><span data-stu-id="4cabd-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="4cabd-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4cabd-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="4cabd-113">Usuwa definicję rejestracji dla danego obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="4cabd-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="4cabd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cabd-114">PARAMETERS</span></span>

### <span data-ttu-id="4cabd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cabd-115">-DefaultProfile</span></span>
<span data-ttu-id="4cabd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cabd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cabd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cabd-117">-InputObject</span></span>
<span data-ttu-id="4cabd-118">Obiekt definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cabd-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cabd-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cabd-119">-Name</span></span>
<span data-ttu-id="4cabd-120">Unikatowa nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cabd-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cabd-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="4cabd-121">-Scope</span></span>
<span data-ttu-id="4cabd-122">Zakres utworzenia definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cabd-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cabd-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cabd-123">-Confirm</span></span>
<span data-ttu-id="4cabd-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cabd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cabd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cabd-125">-WhatIf</span></span>
<span data-ttu-id="4cabd-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cabd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cabd-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cabd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cabd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cabd-128">CommonParameters</span></span>
<span data-ttu-id="4cabd-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cabd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cabd-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cabd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cabd-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cabd-131">INPUTS</span></span>

### <span data-ttu-id="4cabd-132">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="4cabd-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="4cabd-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4cabd-133">OUTPUTS</span></span>

### <span data-ttu-id="4cabd-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="4cabd-134">System.Void</span></span>
## <span data-ttu-id="4cabd-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cabd-135">NOTES</span></span>

## <span data-ttu-id="4cabd-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cabd-136">RELATED LINKS</span></span>
