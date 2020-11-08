---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063782"
---
# <span data-ttu-id="38894-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="38894-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38894-102">SYNOPSIS</span></span>
<span data-ttu-id="38894-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="38894-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="38894-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38894-104">SYNTAX</span></span>

### <span data-ttu-id="38894-105">S1</span><span class="sxs-lookup"><span data-stu-id="38894-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38894-106">S2</span><span class="sxs-lookup"><span data-stu-id="38894-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38894-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38894-107">DESCRIPTION</span></span>
<span data-ttu-id="38894-108">Polecenie cmdlet **Remove-AzWebApp** usuwa aplikację Azure Web App, która dostarczyła grupę zasobów i nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="38894-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="38894-109">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="38894-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="38894-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38894-110">EXAMPLES</span></span>

### <span data-ttu-id="38894-111">Przykład 1: Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="38894-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="38894-112">To polecenie powoduje usunięcie aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="38894-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="38894-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38894-113">PARAMETERS</span></span>

### <span data-ttu-id="38894-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38894-114">-AsJob</span></span>
<span data-ttu-id="38894-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="38894-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38894-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38894-116">-DefaultProfile</span></span>
<span data-ttu-id="38894-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38894-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38894-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38894-118">-Force</span></span>
<span data-ttu-id="38894-119">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="38894-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="38894-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38894-120">-Name</span></span>
<span data-ttu-id="38894-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="38894-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38894-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38894-122">-ResourceGroupName</span></span>
<span data-ttu-id="38894-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="38894-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38894-124">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="38894-124">-WebApp</span></span>
<span data-ttu-id="38894-125">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="38894-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38894-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38894-126">-Confirm</span></span>
<span data-ttu-id="38894-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet. Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38894-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38894-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38894-128">-WhatIf</span></span>
<span data-ttu-id="38894-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38894-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38894-130">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38894-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38894-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38894-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38894-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38894-132">CommonParameters</span></span>
<span data-ttu-id="38894-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38894-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38894-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38894-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38894-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38894-135">INPUTS</span></span>

### <span data-ttu-id="38894-136">System. String</span><span class="sxs-lookup"><span data-stu-id="38894-136">System.String</span></span>

### <span data-ttu-id="38894-137">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="38894-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="38894-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38894-138">OUTPUTS</span></span>

### <span data-ttu-id="38894-139">System. void</span><span class="sxs-lookup"><span data-stu-id="38894-139">System.Void</span></span>

## <span data-ttu-id="38894-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38894-140">NOTES</span></span>

## <span data-ttu-id="38894-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38894-141">RELATED LINKS</span></span>

[<span data-ttu-id="38894-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="38894-143">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="38894-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="38894-145">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="38894-146">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="38894-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


