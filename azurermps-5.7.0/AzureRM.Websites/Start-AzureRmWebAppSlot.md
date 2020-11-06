---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: e9b0fa9f492c64f86668688d12171795735a46dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524778"
---
# <span data-ttu-id="7de67-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7de67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7de67-102">SYNOPSIS</span></span>
<span data-ttu-id="7de67-103">Uruchamia miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7de67-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7de67-104">SYNTAX</span></span>

### <span data-ttu-id="7de67-105">S1</span><span class="sxs-lookup"><span data-stu-id="7de67-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7de67-106">S2</span><span class="sxs-lookup"><span data-stu-id="7de67-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de67-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7de67-107">DESCRIPTION</span></span>
<span data-ttu-id="7de67-108">Polecenie cmdlet **Start-AzureRmWebAppSlot** uruchamia miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7de67-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="7de67-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7de67-109">EXAMPLES</span></span>

### <span data-ttu-id="7de67-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7de67-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="7de67-111">To polecenie umożliwia uruchomienie gniazda o nazwie Slot001 należącego do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="7de67-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7de67-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7de67-112">PARAMETERS</span></span>

### <span data-ttu-id="7de67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de67-113">-DefaultProfile</span></span>
<span data-ttu-id="7de67-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7de67-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de67-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7de67-115">-Name</span></span>
<span data-ttu-id="7de67-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7de67-116">WebApp Name</span></span>

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

### <span data-ttu-id="7de67-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de67-117">-ResourceGroupName</span></span>
<span data-ttu-id="7de67-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7de67-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7de67-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="7de67-119">-Slot</span></span>
<span data-ttu-id="7de67-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="7de67-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de67-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7de67-121">-WebApp</span></span>
<span data-ttu-id="7de67-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7de67-122">WebApp Object</span></span>

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

### <span data-ttu-id="7de67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de67-123">CommonParameters</span></span>
<span data-ttu-id="7de67-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de67-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de67-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de67-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7de67-126">INPUTS</span></span>

### <span data-ttu-id="7de67-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="7de67-127">Site</span></span>
<span data-ttu-id="7de67-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7de67-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7de67-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7de67-129">OUTPUTS</span></span>

## <span data-ttu-id="7de67-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7de67-130">NOTES</span></span>

## <span data-ttu-id="7de67-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7de67-131">RELATED LINKS</span></span>

[<span data-ttu-id="7de67-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-133">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-137">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7de67-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="7de67-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7de67-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
