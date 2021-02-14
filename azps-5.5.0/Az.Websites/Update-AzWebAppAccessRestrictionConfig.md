---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241498"
---
# <span data-ttu-id="48d82-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="48d82-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="48d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48d82-102">SYNOPSIS</span></span>
<span data-ttu-id="48d82-103">Aktualizuje dziedziczenie konfiguracji usługi Restiction programu Access w witrynie programu SCM dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="48d82-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="48d82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48d82-104">SYNTAX</span></span>

### <span data-ttu-id="48d82-105">InputValuesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="48d82-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d82-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48d82-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d82-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="48d82-107">DESCRIPTION</span></span>
<span data-ttu-id="48d82-108">Polecenie **cmdlet Update-AzWebAppAccessRestrictionConfig** aktualizuje konfigurację ograniczeń dostępu dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="48d82-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="48d82-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48d82-109">EXAMPLES</span></span>

### <span data-ttu-id="48d82-110">Przykład 1. Aktualizowanie witryny usługi SCM aplikacji sieci Web w celu stosowania ograniczeń dostępu z witryny głównej</span><span class="sxs-lookup"><span data-stu-id="48d82-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="48d82-111">W poniższym przykładzie aplikacja Sieci Web o nazwie IpRule należąca do grupy zasobów MyResourceGroup używa konfiguracji ograniczeń dostępu witryny głównej w witrynie scm.</span><span class="sxs-lookup"><span data-stu-id="48d82-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="48d82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48d82-112">PARAMETERS</span></span>

### <span data-ttu-id="48d82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d82-113">-DefaultProfile</span></span>
<span data-ttu-id="48d82-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48d82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d82-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d82-115">-InputObject</span></span>
<span data-ttu-id="48d82-116">Obiekt konfiguracji ograniczeń dostępu</span><span class="sxs-lookup"><span data-stu-id="48d82-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48d82-117">-Name</span></span>
<span data-ttu-id="48d82-118">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="48d82-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48d82-119">-PassThru</span></span>
<span data-ttu-id="48d82-120">Zwróć obiekt konfiguracji ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="48d82-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="48d82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d82-121">-ResourceGroupName</span></span>
<span data-ttu-id="48d82-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="48d82-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="48d82-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="48d82-124">Witryna scm dziedziczy reguły ustawione w witrynie głównej.</span><span class="sxs-lookup"><span data-stu-id="48d82-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="48d82-125">-SlotName</span></span>
<span data-ttu-id="48d82-126">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="48d82-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d82-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48d82-127">-Confirm</span></span>
<span data-ttu-id="48d82-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48d82-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d82-129">-WhatIf</span></span>
<span data-ttu-id="48d82-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48d82-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48d82-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48d82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d82-132">CommonParameters</span></span>
<span data-ttu-id="48d82-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d82-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48d82-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d82-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48d82-135">INPUTS</span></span>

### <span data-ttu-id="48d82-136">System.String</span><span class="sxs-lookup"><span data-stu-id="48d82-136">System.String</span></span>

### <span data-ttu-id="48d82-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="48d82-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48d82-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48d82-138">OUTPUTS</span></span>

### <span data-ttu-id="48d82-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="48d82-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="48d82-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48d82-140">NOTES</span></span>

## <span data-ttu-id="48d82-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48d82-141">RELATED LINKS</span></span>

[<span data-ttu-id="48d82-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="48d82-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="48d82-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="48d82-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="48d82-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="48d82-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
