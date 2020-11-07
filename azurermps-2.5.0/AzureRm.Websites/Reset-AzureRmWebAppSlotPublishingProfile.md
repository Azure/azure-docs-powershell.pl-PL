---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899182"
---
# <span data-ttu-id="29a06-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="29a06-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="29a06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29a06-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29a06-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29a06-103">SYNTAX</span></span>

### <span data-ttu-id="29a06-104">S1</span><span class="sxs-lookup"><span data-stu-id="29a06-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29a06-105">S2</span><span class="sxs-lookup"><span data-stu-id="29a06-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29a06-106">Opis</span><span class="sxs-lookup"><span data-stu-id="29a06-106">DESCRIPTION</span></span>
<span data-ttu-id="29a06-107">Polecenie cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="29a06-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="29a06-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29a06-108">EXAMPLES</span></span>

### <span data-ttu-id="29a06-109">1:1</span><span class="sxs-lookup"><span data-stu-id="29a06-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="29a06-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="29a06-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="29a06-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29a06-111">PARAMETERS</span></span>

### <span data-ttu-id="29a06-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a06-112">-DefaultProfile</span></span>
<span data-ttu-id="29a06-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29a06-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29a06-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29a06-114">-Name</span></span>
<span data-ttu-id="29a06-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="29a06-115">WebApp Name</span></span>

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

### <span data-ttu-id="29a06-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a06-116">-ResourceGroupName</span></span>
<span data-ttu-id="29a06-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="29a06-117">Resource Group Name</span></span>

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

### <span data-ttu-id="29a06-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="29a06-118">-Slot</span></span>
<span data-ttu-id="29a06-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="29a06-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="29a06-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="29a06-120">-WebApp</span></span>
<span data-ttu-id="29a06-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="29a06-121">WebApp Object</span></span>

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

### <span data-ttu-id="29a06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a06-122">CommonParameters</span></span>
<span data-ttu-id="29a06-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a06-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a06-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a06-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29a06-125">INPUTS</span></span>

### <span data-ttu-id="29a06-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="29a06-126">Site</span></span>
<span data-ttu-id="29a06-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="29a06-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="29a06-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29a06-128">OUTPUTS</span></span>

## <span data-ttu-id="29a06-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29a06-129">NOTES</span></span>

## <span data-ttu-id="29a06-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29a06-130">RELATED LINKS</span></span>

