---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553723"
---
# <span data-ttu-id="13429-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="13429-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13429-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13429-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13429-103">SYNTAX</span></span>

### <span data-ttu-id="13429-104">S1</span><span class="sxs-lookup"><span data-stu-id="13429-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13429-105">S2</span><span class="sxs-lookup"><span data-stu-id="13429-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13429-106">Opis</span><span class="sxs-lookup"><span data-stu-id="13429-106">DESCRIPTION</span></span>
<span data-ttu-id="13429-107">Polecenie cmdlet **Remove-AzureRmWebAppSlot** usuwa miejsce w usłudze Azure Web App, pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="13429-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="13429-108">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="13429-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="13429-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13429-109">EXAMPLES</span></span>

### <span data-ttu-id="13429-110">Przykład 1. Usuń miejsce aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="13429-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="13429-111">To polecenie powoduje usunięcie gniazda o nazwie Slot001 skojarzonego z aplikacją sieci Web ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="13429-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="13429-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13429-112">PARAMETERS</span></span>

### <span data-ttu-id="13429-113">-Force</span><span class="sxs-lookup"><span data-stu-id="13429-113">-Force</span></span>
<span data-ttu-id="13429-114">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="13429-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="13429-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13429-115">-Name</span></span>
<span data-ttu-id="13429-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="13429-116">WebApp Name</span></span>

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

### <span data-ttu-id="13429-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13429-117">-ResourceGroupName</span></span>
<span data-ttu-id="13429-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="13429-118">Resource Group Name</span></span>

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

### <span data-ttu-id="13429-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="13429-119">-Slot</span></span>
<span data-ttu-id="13429-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="13429-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13429-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="13429-121">-WebApp</span></span>
<span data-ttu-id="13429-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="13429-122">WebApp Object</span></span>

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

### <span data-ttu-id="13429-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13429-123">-Confirm</span></span>
<span data-ttu-id="13429-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13429-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13429-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13429-125">-WhatIf</span></span>
<span data-ttu-id="13429-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13429-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13429-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13429-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13429-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13429-128">-DefaultProfile</span></span>
<span data-ttu-id="13429-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13429-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13429-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13429-130">CommonParameters</span></span>
<span data-ttu-id="13429-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13429-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13429-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13429-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13429-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13429-133">INPUTS</span></span>

### <span data-ttu-id="13429-134">Klienta</span><span class="sxs-lookup"><span data-stu-id="13429-134">Site</span></span>
<span data-ttu-id="13429-135">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="13429-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="13429-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13429-136">OUTPUTS</span></span>

### <span data-ttu-id="13429-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13429-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="13429-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13429-138">NOTES</span></span>

## <span data-ttu-id="13429-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13429-139">RELATED LINKS</span></span>

[<span data-ttu-id="13429-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-141">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-142">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-144">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-145">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13429-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="13429-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="13429-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
