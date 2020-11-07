---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: e7c0d37dc56e1ff4c986aa66632dccddec283c83
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899024"
---
# <span data-ttu-id="56d13-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="56d13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56d13-102">SYNOPSIS</span></span>
<span data-ttu-id="56d13-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="56d13-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56d13-104">SYNTAX</span></span>

### <span data-ttu-id="56d13-105">S1</span><span class="sxs-lookup"><span data-stu-id="56d13-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d13-106">S2</span><span class="sxs-lookup"><span data-stu-id="56d13-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56d13-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56d13-107">DESCRIPTION</span></span>
<span data-ttu-id="56d13-108">Polecenie cmdlet **Remove-AzureRmWebApp** usuwa aplikację Azure Web App, która dostarczyła grupę zasobów i nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="56d13-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="56d13-109">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="56d13-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="56d13-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56d13-110">EXAMPLES</span></span>

### <span data-ttu-id="56d13-111">Przykład 1: Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="56d13-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="56d13-112">To polecenie powoduje usunięcie aplikacji Azure Web App o nazwie ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="56d13-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="56d13-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56d13-113">PARAMETERS</span></span>

### <span data-ttu-id="56d13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d13-114">-DefaultProfile</span></span>
<span data-ttu-id="56d13-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56d13-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-116">-Force</span><span class="sxs-lookup"><span data-stu-id="56d13-116">-Force</span></span>
<span data-ttu-id="56d13-117">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="56d13-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56d13-118">-Name</span></span>
<span data-ttu-id="56d13-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="56d13-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d13-120">-ResourceGroupName</span></span>
<span data-ttu-id="56d13-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="56d13-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="56d13-122">-WebApp</span></span>
<span data-ttu-id="56d13-123">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="56d13-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56d13-124">-Confirm</span></span>
<span data-ttu-id="56d13-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet. Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d13-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d13-126">-WhatIf</span></span>
<span data-ttu-id="56d13-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d13-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d13-128">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d13-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d13-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56d13-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56d13-130">-AsJob</span></span>
<span data-ttu-id="56d13-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="56d13-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d13-132">CommonParameters</span></span>
<span data-ttu-id="56d13-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d13-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d13-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56d13-135">INPUTS</span></span>

### <span data-ttu-id="56d13-136">Klienta</span><span class="sxs-lookup"><span data-stu-id="56d13-136">Site</span></span>
<span data-ttu-id="56d13-137">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="56d13-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56d13-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56d13-138">OUTPUTS</span></span>

## <span data-ttu-id="56d13-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56d13-139">NOTES</span></span>

## <span data-ttu-id="56d13-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56d13-140">RELATED LINKS</span></span>

[<span data-ttu-id="56d13-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="56d13-142">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="56d13-143">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="56d13-144">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="56d13-145">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56d13-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


