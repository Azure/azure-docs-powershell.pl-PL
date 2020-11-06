---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525882"
---
# <span data-ttu-id="fa0ef-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="fa0ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0ef-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa0ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa0ef-104">SYNTAX</span></span>

### <span data-ttu-id="fa0ef-105">S1</span><span class="sxs-lookup"><span data-stu-id="fa0ef-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0ef-106">S2</span><span class="sxs-lookup"><span data-stu-id="fa0ef-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa0ef-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0ef-108">Polecenie cmdlet **Remove-AzureRmWebApp** usuwa aplikację Azure Web App, która dostarczyła grupę zasobów i nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="fa0ef-109">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="fa0ef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa0ef-110">EXAMPLES</span></span>

### <span data-ttu-id="fa0ef-111">Przykład 1: Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="fa0ef-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fa0ef-112">To polecenie powoduje usunięcie aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fa0ef-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa0ef-113">PARAMETERS</span></span>

### <span data-ttu-id="fa0ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa0ef-114">-AsJob</span></span>
<span data-ttu-id="fa0ef-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fa0ef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa0ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0ef-116">-DefaultProfile</span></span>
<span data-ttu-id="fa0ef-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa0ef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa0ef-118">-Force</span></span>
<span data-ttu-id="fa0ef-119">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="fa0ef-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="fa0ef-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa0ef-120">-Name</span></span>
<span data-ttu-id="fa0ef-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa0ef-121">WebApp Name</span></span>

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

### <span data-ttu-id="fa0ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa0ef-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fa0ef-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fa0ef-124">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa0ef-124">-WebApp</span></span>
<span data-ttu-id="fa0ef-125">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa0ef-125">WebApp Object</span></span>

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

### <span data-ttu-id="fa0ef-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa0ef-126">-Confirm</span></span>
<span data-ttu-id="fa0ef-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet. Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0ef-128">-WhatIf</span></span>
<span data-ttu-id="fa0ef-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0ef-130">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0ef-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0ef-132">CommonParameters</span></span>
<span data-ttu-id="fa0ef-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa0ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0ef-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0ef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0ef-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa0ef-135">INPUTS</span></span>

### <span data-ttu-id="fa0ef-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0ef-136">System.String</span></span>

### <span data-ttu-id="fa0ef-137">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="fa0ef-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="fa0ef-138">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa0ef-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="fa0ef-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa0ef-139">OUTPUTS</span></span>

### <span data-ttu-id="fa0ef-140">System. void</span><span class="sxs-lookup"><span data-stu-id="fa0ef-140">System.Void</span></span>

## <span data-ttu-id="fa0ef-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa0ef-141">NOTES</span></span>

## <span data-ttu-id="fa0ef-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa0ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="fa0ef-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="fa0ef-144">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="fa0ef-145">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="fa0ef-146">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="fa0ef-147">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fa0ef-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


