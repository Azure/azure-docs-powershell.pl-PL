---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990697"
---
# <span data-ttu-id="3a81e-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a81e-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="3a81e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a81e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a81e-103">Usuń regułę routingu z gniazda.</span><span class="sxs-lookup"><span data-stu-id="3a81e-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="3a81e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a81e-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a81e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a81e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a81e-106">Polecenie **cmdlet Remove-AzWebAppTrafficRouting** usuwa regułę routingu z gniazda aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3a81e-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="3a81e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a81e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a81e-108">Przykład 1. Usunięcie określonej reguły routingu z gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="3a81e-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="3a81e-109">To polecenie usuwa regułę routingu dla danego gniazda aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="3a81e-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="3a81e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a81e-110">PARAMETERS</span></span>

### <span data-ttu-id="3a81e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a81e-111">-DefaultProfile</span></span>
<span data-ttu-id="3a81e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a81e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a81e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a81e-113">-ResourceGroupName</span></span>
<span data-ttu-id="3a81e-114">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3a81e-114">Resource Group Name</span></span>

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

### <span data-ttu-id="3a81e-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3a81e-115">-RuleName</span></span>
<span data-ttu-id="3a81e-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="3a81e-116">Rule Name</span></span>

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

### <span data-ttu-id="3a81e-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3a81e-117">-WebAppName</span></span>
<span data-ttu-id="3a81e-118">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="3a81e-118">WebApp Name</span></span>

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

### <span data-ttu-id="3a81e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a81e-119">-PassThru</span></span>
<span data-ttu-id="3a81e-120">Zwróć obiekt konfiguracji ograniczeń dostępu.</span><span class="sxs-lookup"><span data-stu-id="3a81e-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="3a81e-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a81e-121">-Confirm</span></span>
<span data-ttu-id="3a81e-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a81e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a81e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a81e-123">-WhatIf</span></span>
<span data-ttu-id="3a81e-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a81e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a81e-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a81e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a81e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a81e-126">CommonParameters</span></span>
<span data-ttu-id="3a81e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a81e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a81e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a81e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a81e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a81e-129">INPUTS</span></span>

### <span data-ttu-id="3a81e-130">Brak</span><span class="sxs-lookup"><span data-stu-id="3a81e-130">None</span></span>

## <span data-ttu-id="3a81e-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a81e-131">OUTPUTS</span></span>

### <span data-ttu-id="3a81e-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="3a81e-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="3a81e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a81e-133">NOTES</span></span>

## <span data-ttu-id="3a81e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a81e-134">RELATED LINKS</span></span>
[<span data-ttu-id="3a81e-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a81e-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3a81e-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a81e-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3a81e-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a81e-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)