---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 948088f99e90af4594e239dc379133955340e1d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546319"
---
# <span data-ttu-id="c14ee-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c14ee-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="c14ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c14ee-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c14ee-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c14ee-103">SYNTAX</span></span>

### <span data-ttu-id="c14ee-104">S1</span><span class="sxs-lookup"><span data-stu-id="c14ee-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14ee-105">S2</span><span class="sxs-lookup"><span data-stu-id="c14ee-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c14ee-106">Opis</span><span class="sxs-lookup"><span data-stu-id="c14ee-106">DESCRIPTION</span></span>
<span data-ttu-id="c14ee-107">Polecenie cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c14ee-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="c14ee-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c14ee-108">EXAMPLES</span></span>

### <span data-ttu-id="c14ee-109">1:1</span><span class="sxs-lookup"><span data-stu-id="c14ee-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="c14ee-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c14ee-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c14ee-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c14ee-111">PARAMETERS</span></span>

### <span data-ttu-id="c14ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14ee-112">-DefaultProfile</span></span>
<span data-ttu-id="c14ee-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c14ee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c14ee-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c14ee-114">-Name</span></span>
<span data-ttu-id="c14ee-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c14ee-115">WebApp Name</span></span>

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

### <span data-ttu-id="c14ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="c14ee-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c14ee-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c14ee-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="c14ee-118">-Slot</span></span>
<span data-ttu-id="c14ee-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="c14ee-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c14ee-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c14ee-120">-WebApp</span></span>
<span data-ttu-id="c14ee-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c14ee-121">WebApp Object</span></span>

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

### <span data-ttu-id="c14ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14ee-122">CommonParameters</span></span>
<span data-ttu-id="c14ee-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14ee-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14ee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14ee-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c14ee-125">INPUTS</span></span>

### <span data-ttu-id="c14ee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c14ee-126">System.String</span></span>

### <span data-ttu-id="c14ee-127">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="c14ee-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c14ee-128">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c14ee-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c14ee-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c14ee-129">OUTPUTS</span></span>

### <span data-ttu-id="c14ee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c14ee-130">System.String</span></span>

## <span data-ttu-id="c14ee-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c14ee-131">NOTES</span></span>

## <span data-ttu-id="c14ee-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c14ee-132">RELATED LINKS</span></span>
