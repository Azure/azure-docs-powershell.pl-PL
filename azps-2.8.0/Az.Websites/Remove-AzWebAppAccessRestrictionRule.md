---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888589"
---
# <span data-ttu-id="09d2c-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="09d2c-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="09d2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="09d2c-103">Usuwa regułę ograniczeń dostępu z aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="09d2c-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="09d2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09d2c-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="09d2c-106">Polecenie cmdlet **Remove-AzWebAppAccessRestrictionRule** usuwa regułę ograniczeń programu Access z aplikacji sieci Web platformy Azure</span><span class="sxs-lookup"><span data-stu-id="09d2c-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="09d2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="09d2c-108">Przykład 1: Usuwanie reguły ograniczenia dostępu aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="09d2c-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="09d2c-109">To polecenie usuwa regułę ograniczenia dostępu IpRule z aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="09d2c-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="09d2c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09d2c-110">PARAMETERS</span></span>

### <span data-ttu-id="09d2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d2c-111">-DefaultProfile</span></span>
<span data-ttu-id="09d2c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09d2c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d2c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09d2c-113">-Name</span></span>
<span data-ttu-id="09d2c-114">Nazwa reguły ograniczeń dostępu</span><span class="sxs-lookup"><span data-stu-id="09d2c-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d2c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09d2c-115">-PassThru</span></span>
<span data-ttu-id="09d2c-116">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="09d2c-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="09d2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="09d2c-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09d2c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d2c-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="09d2c-119">-SlotName</span></span>
<span data-ttu-id="09d2c-120">Nazwa miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="09d2c-120">Deployment Slot Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d2c-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="09d2c-121">-TargetScmSite</span></span>
<span data-ttu-id="09d2c-122">Reguła ma na celu witrynę główną witryny lub SCM.</span><span class="sxs-lookup"><span data-stu-id="09d2c-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="09d2c-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="09d2c-123">-WebAppName</span></span>
<span data-ttu-id="09d2c-124">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="09d2c-124">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d2c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09d2c-125">-Confirm</span></span>
<span data-ttu-id="09d2c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09d2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d2c-127">-WhatIf</span></span>
<span data-ttu-id="09d2c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d2c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09d2c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09d2c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09d2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d2c-130">CommonParameters</span></span>
<span data-ttu-id="09d2c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d2c-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09d2c-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d2c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09d2c-133">INPUTS</span></span>

### <span data-ttu-id="09d2c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="09d2c-134">System.String</span></span>

## <span data-ttu-id="09d2c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09d2c-135">OUTPUTS</span></span>

### <span data-ttu-id="09d2c-136">Microsoft. Azure. Commands. webapps. modele. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="09d2c-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="09d2c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09d2c-137">NOTES</span></span>

## <span data-ttu-id="09d2c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09d2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="09d2c-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="09d2c-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="09d2c-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="09d2c-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="09d2c-141">Dodaj-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="09d2c-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
