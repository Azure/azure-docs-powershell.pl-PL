---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063769"
---
# <span data-ttu-id="85736-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85736-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="85736-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85736-102">SYNOPSIS</span></span>
<span data-ttu-id="85736-103">Usuwanie reguły routingu z gniazda.</span><span class="sxs-lookup"><span data-stu-id="85736-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="85736-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85736-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85736-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85736-105">DESCRIPTION</span></span>
<span data-ttu-id="85736-106">Polecenie cmdlet **Remove-AzWebAppTrafficRouting** usuwa regułę routingu z miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="85736-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="85736-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85736-107">EXAMPLES</span></span>

### <span data-ttu-id="85736-108">Przykład 1 usuwa określoną regułę routingu z gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="85736-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="85736-109">To polecenie usuwa regułę routingu dla danego gniazda aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85736-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="85736-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85736-110">PARAMETERS</span></span>

### <span data-ttu-id="85736-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85736-111">-DefaultProfile</span></span>
<span data-ttu-id="85736-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85736-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85736-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85736-113">-ResourceGroupName</span></span>
<span data-ttu-id="85736-114">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85736-114">Resource Group Name</span></span>

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

### <span data-ttu-id="85736-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="85736-115">-RuleName</span></span>
<span data-ttu-id="85736-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="85736-116">Rule Name</span></span>

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

### <span data-ttu-id="85736-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="85736-117">-WebAppName</span></span>
<span data-ttu-id="85736-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="85736-118">WebApp Name</span></span>

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

### <span data-ttu-id="85736-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85736-119">-PassThru</span></span>
<span data-ttu-id="85736-120">Zwracanie obiektu konfiguracji ograniczenia dostępu.</span><span class="sxs-lookup"><span data-stu-id="85736-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="85736-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85736-121">-Confirm</span></span>
<span data-ttu-id="85736-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85736-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85736-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85736-123">-WhatIf</span></span>
<span data-ttu-id="85736-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85736-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85736-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85736-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85736-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85736-126">CommonParameters</span></span>
<span data-ttu-id="85736-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85736-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85736-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85736-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85736-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85736-129">INPUTS</span></span>

### <span data-ttu-id="85736-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85736-130">None</span></span>

## <span data-ttu-id="85736-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85736-131">OUTPUTS</span></span>

### <span data-ttu-id="85736-132">Microsoft. Azure. Management. Web. MODELES. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="85736-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="85736-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85736-133">NOTES</span></span>

## <span data-ttu-id="85736-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85736-134">RELATED LINKS</span></span>
[<span data-ttu-id="85736-135">Dodaj-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85736-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="85736-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85736-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="85736-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="85736-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)