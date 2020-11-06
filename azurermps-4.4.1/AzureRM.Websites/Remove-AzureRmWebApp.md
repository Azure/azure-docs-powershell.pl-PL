---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553726"
---
# <span data-ttu-id="7eb87-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="7eb87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7eb87-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb87-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7eb87-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7eb87-104">SYNTAX</span></span>

### <span data-ttu-id="7eb87-105">S1</span><span class="sxs-lookup"><span data-stu-id="7eb87-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb87-106">S2</span><span class="sxs-lookup"><span data-stu-id="7eb87-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eb87-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7eb87-107">DESCRIPTION</span></span>
<span data-ttu-id="7eb87-108">Polecenie cmdlet **Remove-AzureRmWebApp** usuwa aplikację Azure Web App, która dostarczyła grupę zasobów i nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7eb87-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="7eb87-109">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="7eb87-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="7eb87-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7eb87-110">EXAMPLES</span></span>

### <span data-ttu-id="7eb87-111">Przykład 1: Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="7eb87-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7eb87-112">To polecenie powoduje usunięcie aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="7eb87-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7eb87-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7eb87-113">PARAMETERS</span></span>

### <span data-ttu-id="7eb87-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7eb87-114">-Force</span></span>
<span data-ttu-id="7eb87-115">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="7eb87-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="7eb87-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7eb87-116">-Name</span></span>
<span data-ttu-id="7eb87-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7eb87-117">WebApp Name</span></span>

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

### <span data-ttu-id="7eb87-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb87-118">-ResourceGroupName</span></span>
<span data-ttu-id="7eb87-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7eb87-119">Resource Group Name</span></span>

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

### <span data-ttu-id="7eb87-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7eb87-120">-WebApp</span></span>
<span data-ttu-id="7eb87-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7eb87-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb87-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7eb87-122">-Confirm</span></span>
<span data-ttu-id="7eb87-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet. Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb87-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb87-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb87-124">-WhatIf</span></span>
<span data-ttu-id="7eb87-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb87-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb87-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb87-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb87-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7eb87-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb87-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb87-128">-DefaultProfile</span></span>
<span data-ttu-id="7eb87-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb87-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eb87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb87-130">CommonParameters</span></span>
<span data-ttu-id="7eb87-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb87-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb87-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb87-133">INPUTS</span></span>

### <span data-ttu-id="7eb87-134">Klienta</span><span class="sxs-lookup"><span data-stu-id="7eb87-134">Site</span></span>
<span data-ttu-id="7eb87-135">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7eb87-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7eb87-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7eb87-136">OUTPUTS</span></span>

## <span data-ttu-id="7eb87-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7eb87-137">NOTES</span></span>

## <span data-ttu-id="7eb87-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb87-138">RELATED LINKS</span></span>

[<span data-ttu-id="7eb87-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7eb87-140">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="7eb87-141">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7eb87-142">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7eb87-143">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7eb87-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


