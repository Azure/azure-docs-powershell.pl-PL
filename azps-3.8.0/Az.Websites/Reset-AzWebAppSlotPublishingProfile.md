---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 8670581b376fe185ae4e477524f8f0a01c7cd3a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051882"
---
# <span data-ttu-id="70e49-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="70e49-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="70e49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70e49-102">SYNOPSIS</span></span>

## <span data-ttu-id="70e49-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70e49-103">SYNTAX</span></span>

### <span data-ttu-id="70e49-104">S1</span><span class="sxs-lookup"><span data-stu-id="70e49-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70e49-105">S2</span><span class="sxs-lookup"><span data-stu-id="70e49-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70e49-106">Opis</span><span class="sxs-lookup"><span data-stu-id="70e49-106">DESCRIPTION</span></span>
<span data-ttu-id="70e49-107">Polecenie cmdlet **Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="70e49-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="70e49-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70e49-108">EXAMPLES</span></span>

### <span data-ttu-id="70e49-109">1:1</span><span class="sxs-lookup"><span data-stu-id="70e49-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="70e49-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="70e49-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="70e49-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70e49-111">PARAMETERS</span></span>

### <span data-ttu-id="70e49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e49-112">-DefaultProfile</span></span>
<span data-ttu-id="70e49-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70e49-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e49-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70e49-114">-Name</span></span>
<span data-ttu-id="70e49-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="70e49-115">WebApp Name</span></span>

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

### <span data-ttu-id="70e49-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e49-116">-ResourceGroupName</span></span>
<span data-ttu-id="70e49-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="70e49-117">Resource Group Name</span></span>

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

### <span data-ttu-id="70e49-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="70e49-118">-Slot</span></span>
<span data-ttu-id="70e49-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="70e49-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="70e49-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="70e49-120">-WebApp</span></span>
<span data-ttu-id="70e49-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="70e49-121">WebApp Object</span></span>

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

### <span data-ttu-id="70e49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e49-122">CommonParameters</span></span>
<span data-ttu-id="70e49-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e49-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e49-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e49-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70e49-125">INPUTS</span></span>

### <span data-ttu-id="70e49-126">System. String</span><span class="sxs-lookup"><span data-stu-id="70e49-126">System.String</span></span>

### <span data-ttu-id="70e49-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="70e49-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="70e49-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70e49-128">OUTPUTS</span></span>

### <span data-ttu-id="70e49-129">System. String</span><span class="sxs-lookup"><span data-stu-id="70e49-129">System.String</span></span>

## <span data-ttu-id="70e49-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70e49-130">NOTES</span></span>

## <span data-ttu-id="70e49-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70e49-131">RELATED LINKS</span></span>
