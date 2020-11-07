---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 97bf4078ca09ce250fea0d7c660629fbab651974
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898845"
---
# <span data-ttu-id="87cd8-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="87cd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="87cd8-103">Uruchamia miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="87cd8-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87cd8-104">SYNTAX</span></span>

### <span data-ttu-id="87cd8-105">S1</span><span class="sxs-lookup"><span data-stu-id="87cd8-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cd8-106">S2</span><span class="sxs-lookup"><span data-stu-id="87cd8-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cd8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87cd8-107">DESCRIPTION</span></span>
<span data-ttu-id="87cd8-108">Polecenie cmdlet **Start-AzureRmWebAppSlot** uruchamia miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87cd8-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="87cd8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87cd8-109">EXAMPLES</span></span>

### <span data-ttu-id="87cd8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87cd8-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="87cd8-111">To polecenie umożliwia uruchomienie gniazda o nazwie Slot001 należącego do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="87cd8-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="87cd8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87cd8-112">PARAMETERS</span></span>

### <span data-ttu-id="87cd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cd8-113">-DefaultProfile</span></span>
<span data-ttu-id="87cd8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87cd8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87cd8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87cd8-115">-Name</span></span>
<span data-ttu-id="87cd8-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="87cd8-116">WebApp Name</span></span>

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

### <span data-ttu-id="87cd8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87cd8-117">-ResourceGroupName</span></span>
<span data-ttu-id="87cd8-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="87cd8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="87cd8-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="87cd8-119">-Slot</span></span>
<span data-ttu-id="87cd8-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="87cd8-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="87cd8-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="87cd8-121">-WebApp</span></span>
<span data-ttu-id="87cd8-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="87cd8-122">WebApp Object</span></span>

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

### <span data-ttu-id="87cd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cd8-123">CommonParameters</span></span>
<span data-ttu-id="87cd8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87cd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cd8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87cd8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cd8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87cd8-126">INPUTS</span></span>

### <span data-ttu-id="87cd8-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="87cd8-127">Site</span></span>
<span data-ttu-id="87cd8-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="87cd8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="87cd8-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87cd8-129">OUTPUTS</span></span>

## <span data-ttu-id="87cd8-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87cd8-130">NOTES</span></span>

## <span data-ttu-id="87cd8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87cd8-131">RELATED LINKS</span></span>

[<span data-ttu-id="87cd8-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-133">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-137">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="87cd8-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="87cd8-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="87cd8-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
