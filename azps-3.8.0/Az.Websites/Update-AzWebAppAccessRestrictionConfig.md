---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 9069dd055fd3cccdbd1efe520fc560c385d15cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051548"
---
# <span data-ttu-id="44f75-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44f75-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="44f75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44f75-102">SYNOPSIS</span></span>
<span data-ttu-id="44f75-103">Umożliwia zaktualizowanie dziedziczenia witryny sieci Web programu Access restiction config na witrynę SCM.</span><span class="sxs-lookup"><span data-stu-id="44f75-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="44f75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44f75-104">SYNTAX</span></span>

### <span data-ttu-id="44f75-105">InputValuesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44f75-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f75-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44f75-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44f75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44f75-107">DESCRIPTION</span></span>
<span data-ttu-id="44f75-108">Polecenie cmdlet **Update-AzWebAppAccessRestrictionConfig** umożliwia aktualizowanie konfiguracji ograniczeń dotyczących dostępu do aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44f75-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="44f75-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44f75-109">EXAMPLES</span></span>

### <span data-ttu-id="44f75-110">Przykład 1: Aktualizowanie witryny SCM aplikacji sieci Web w celu używania ograniczeń dostępu z witryny głównej</span><span class="sxs-lookup"><span data-stu-id="44f75-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="44f75-111">To polecenie powoduje zaktualizowanie aplikacji sieci Web o nazwie ContosoSite należącej do pozycji domyślne grupy zasobów — sieć Web-zachód, aby używać konfiguracji ograniczeń programu Access witryny głównej w witrynie SCM.</span><span class="sxs-lookup"><span data-stu-id="44f75-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="44f75-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44f75-112">PARAMETERS</span></span>

### <span data-ttu-id="44f75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f75-113">-DefaultProfile</span></span>
<span data-ttu-id="44f75-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44f75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f75-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44f75-115">-InputObject</span></span>
<span data-ttu-id="44f75-116">Obiekt konfiguracji ograniczenia dostępu</span><span class="sxs-lookup"><span data-stu-id="44f75-116">The access restriction config object</span></span>

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

### <span data-ttu-id="44f75-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44f75-117">-Name</span></span>
<span data-ttu-id="44f75-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="44f75-118">WebApp Name</span></span>

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

### <span data-ttu-id="44f75-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44f75-119">-PassThru</span></span>
<span data-ttu-id="44f75-120">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="44f75-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="44f75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f75-121">-ResourceGroupName</span></span>
<span data-ttu-id="44f75-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44f75-122">Resource Group Name</span></span>

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

### <span data-ttu-id="44f75-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44f75-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="44f75-124">Witryna SCM dziedziczy reguły ustawione w witrynie głównej.</span><span class="sxs-lookup"><span data-stu-id="44f75-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="44f75-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="44f75-125">-SlotName</span></span>
<span data-ttu-id="44f75-126">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="44f75-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="44f75-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44f75-127">-Confirm</span></span>
<span data-ttu-id="44f75-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44f75-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44f75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f75-129">-WhatIf</span></span>
<span data-ttu-id="44f75-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44f75-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44f75-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44f75-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44f75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f75-132">CommonParameters</span></span>
<span data-ttu-id="44f75-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f75-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44f75-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f75-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44f75-135">INPUTS</span></span>

### <span data-ttu-id="44f75-136">System. String</span><span class="sxs-lookup"><span data-stu-id="44f75-136">System.String</span></span>

### <span data-ttu-id="44f75-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="44f75-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44f75-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44f75-138">OUTPUTS</span></span>

### <span data-ttu-id="44f75-139">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44f75-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="44f75-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44f75-140">NOTES</span></span>

## <span data-ttu-id="44f75-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44f75-141">RELATED LINKS</span></span>

[<span data-ttu-id="44f75-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44f75-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="44f75-143">Dodaj-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="44f75-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="44f75-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="44f75-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
