---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525874"
---
# <span data-ttu-id="94fbe-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="94fbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="94fbe-103">Uruchamia miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="94fbe-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94fbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94fbe-104">SYNTAX</span></span>

### <span data-ttu-id="94fbe-105">S1</span><span class="sxs-lookup"><span data-stu-id="94fbe-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94fbe-106">S2</span><span class="sxs-lookup"><span data-stu-id="94fbe-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94fbe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="94fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="94fbe-108">Polecenie cmdlet **Start-AzureRmWebAppSlot** uruchamia miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94fbe-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="94fbe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="94fbe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94fbe-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="94fbe-111">To polecenie umożliwia uruchomienie gniazda o nazwie Slot001 należącego do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="94fbe-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="94fbe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94fbe-112">PARAMETERS</span></span>

### <span data-ttu-id="94fbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fbe-113">-DefaultProfile</span></span>
<span data-ttu-id="94fbe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94fbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94fbe-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94fbe-115">-Name</span></span>
<span data-ttu-id="94fbe-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="94fbe-116">WebApp Name</span></span>

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

### <span data-ttu-id="94fbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94fbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="94fbe-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94fbe-118">Resource Group Name</span></span>

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

### <span data-ttu-id="94fbe-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="94fbe-119">-Slot</span></span>
<span data-ttu-id="94fbe-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="94fbe-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="94fbe-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="94fbe-121">-WebApp</span></span>
<span data-ttu-id="94fbe-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="94fbe-122">WebApp Object</span></span>

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

### <span data-ttu-id="94fbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fbe-123">CommonParameters</span></span>
<span data-ttu-id="94fbe-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94fbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fbe-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94fbe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fbe-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94fbe-126">INPUTS</span></span>

### <span data-ttu-id="94fbe-127">System. String</span><span class="sxs-lookup"><span data-stu-id="94fbe-127">System.String</span></span>

### <span data-ttu-id="94fbe-128">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="94fbe-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="94fbe-129">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94fbe-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="94fbe-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94fbe-130">OUTPUTS</span></span>

### <span data-ttu-id="94fbe-131">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="94fbe-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="94fbe-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94fbe-132">NOTES</span></span>

## <span data-ttu-id="94fbe-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94fbe-133">RELATED LINKS</span></span>

[<span data-ttu-id="94fbe-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-135">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-137">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-139">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94fbe-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="94fbe-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94fbe-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
