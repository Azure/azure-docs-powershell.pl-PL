---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898844"
---
# <span data-ttu-id="d5c48-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d5c48-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d5c48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5c48-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c48-103">Zatrzymuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d5c48-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5c48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5c48-104">SYNTAX</span></span>

### <span data-ttu-id="d5c48-105">S1</span><span class="sxs-lookup"><span data-stu-id="d5c48-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c48-106">S2</span><span class="sxs-lookup"><span data-stu-id="d5c48-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c48-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d5c48-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c48-108">Polecenie cmdlet **stop-AzureRmWebAppSlot** zatrzymuje miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c48-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d5c48-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5c48-109">EXAMPLES</span></span>

### <span data-ttu-id="d5c48-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5c48-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d5c48-111">To polecenie zatrzymuje Slot001 miejsca odnoszące się do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="d5c48-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5c48-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5c48-112">PARAMETERS</span></span>

### <span data-ttu-id="d5c48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c48-113">-DefaultProfile</span></span>
<span data-ttu-id="d5c48-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5c48-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5c48-115">-Name</span></span>
<span data-ttu-id="d5c48-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5c48-116">WebApp Name</span></span>

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

### <span data-ttu-id="d5c48-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c48-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5c48-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d5c48-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d5c48-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5c48-119">-Slot</span></span>
<span data-ttu-id="d5c48-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5c48-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d5c48-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5c48-121">-WebApp</span></span>
<span data-ttu-id="d5c48-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5c48-122">WebApp Object</span></span>

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

### <span data-ttu-id="d5c48-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c48-123">CommonParameters</span></span>
<span data-ttu-id="d5c48-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c48-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c48-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c48-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c48-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c48-126">INPUTS</span></span>

### <span data-ttu-id="d5c48-127">Klienta</span><span class="sxs-lookup"><span data-stu-id="d5c48-127">Site</span></span>
<span data-ttu-id="d5c48-128">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="d5c48-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d5c48-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5c48-129">OUTPUTS</span></span>

## <span data-ttu-id="d5c48-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5c48-130">NOTES</span></span>

## <span data-ttu-id="d5c48-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5c48-131">RELATED LINKS</span></span>

