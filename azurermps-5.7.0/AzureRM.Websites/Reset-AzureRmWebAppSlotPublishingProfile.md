---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 352b0bc196745aba3c5eeda357e0727a9ea3e4c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547807"
---
# <span data-ttu-id="a9213-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a9213-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a9213-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9213-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9213-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9213-103">SYNTAX</span></span>

### <span data-ttu-id="a9213-104">S1</span><span class="sxs-lookup"><span data-stu-id="a9213-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9213-105">S2</span><span class="sxs-lookup"><span data-stu-id="a9213-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9213-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a9213-106">DESCRIPTION</span></span>
<span data-ttu-id="a9213-107">Polecenie cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a9213-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a9213-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9213-108">EXAMPLES</span></span>

### <span data-ttu-id="a9213-109">1:1</span><span class="sxs-lookup"><span data-stu-id="a9213-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a9213-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="a9213-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a9213-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9213-111">PARAMETERS</span></span>

### <span data-ttu-id="a9213-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9213-112">-DefaultProfile</span></span>
<span data-ttu-id="a9213-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9213-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9213-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9213-114">-Name</span></span>
<span data-ttu-id="a9213-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9213-115">WebApp Name</span></span>

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

### <span data-ttu-id="a9213-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9213-116">-ResourceGroupName</span></span>
<span data-ttu-id="a9213-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9213-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a9213-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a9213-118">-Slot</span></span>
<span data-ttu-id="a9213-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9213-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a9213-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9213-120">-WebApp</span></span>
<span data-ttu-id="a9213-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9213-121">WebApp Object</span></span>

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

### <span data-ttu-id="a9213-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9213-122">CommonParameters</span></span>
<span data-ttu-id="a9213-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9213-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9213-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9213-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9213-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9213-125">INPUTS</span></span>

### <span data-ttu-id="a9213-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="a9213-126">Site</span></span>
<span data-ttu-id="a9213-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="a9213-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a9213-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9213-128">OUTPUTS</span></span>

## <span data-ttu-id="a9213-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9213-129">NOTES</span></span>

## <span data-ttu-id="a9213-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9213-130">RELATED LINKS</span></span>

