---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: ec0b95ffee67d5597a06ed0729cded33e7489465
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891865"
---
# <span data-ttu-id="ed679-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ed679-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="ed679-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed679-102">SYNOPSIS</span></span>

## <span data-ttu-id="ed679-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed679-103">SYNTAX</span></span>

### <span data-ttu-id="ed679-104">S1</span><span class="sxs-lookup"><span data-stu-id="ed679-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed679-105">S2</span><span class="sxs-lookup"><span data-stu-id="ed679-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed679-106">Opis</span><span class="sxs-lookup"><span data-stu-id="ed679-106">DESCRIPTION</span></span>
<span data-ttu-id="ed679-107">Polecenie cmdlet **Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ed679-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="ed679-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed679-108">EXAMPLES</span></span>

### <span data-ttu-id="ed679-109">1:1</span><span class="sxs-lookup"><span data-stu-id="ed679-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="ed679-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="ed679-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ed679-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed679-111">PARAMETERS</span></span>

### <span data-ttu-id="ed679-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed679-112">-DefaultProfile</span></span>
<span data-ttu-id="ed679-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed679-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed679-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed679-114">-Name</span></span>
<span data-ttu-id="ed679-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="ed679-115">WebApp Name</span></span>

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

### <span data-ttu-id="ed679-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed679-116">-ResourceGroupName</span></span>
<span data-ttu-id="ed679-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ed679-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ed679-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="ed679-118">-Slot</span></span>
<span data-ttu-id="ed679-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="ed679-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ed679-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="ed679-120">-WebApp</span></span>
<span data-ttu-id="ed679-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="ed679-121">WebApp Object</span></span>

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

### <span data-ttu-id="ed679-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed679-122">CommonParameters</span></span>
<span data-ttu-id="ed679-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed679-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed679-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed679-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed679-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed679-125">INPUTS</span></span>

### <span data-ttu-id="ed679-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="ed679-126">Site</span></span>
<span data-ttu-id="ed679-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="ed679-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ed679-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed679-128">OUTPUTS</span></span>

## <span data-ttu-id="ed679-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed679-129">NOTES</span></span>

## <span data-ttu-id="ed679-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed679-130">RELATED LINKS</span></span>

