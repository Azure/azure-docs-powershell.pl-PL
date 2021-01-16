---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326051"
---
# <span data-ttu-id="2f06d-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2f06d-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="2f06d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f06d-102">SYNOPSIS</span></span>

## <span data-ttu-id="2f06d-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f06d-103">SYNTAX</span></span>

### <span data-ttu-id="2f06d-104">S1</span><span class="sxs-lookup"><span data-stu-id="2f06d-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f06d-105">S2</span><span class="sxs-lookup"><span data-stu-id="2f06d-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f06d-106">Opis</span><span class="sxs-lookup"><span data-stu-id="2f06d-106">DESCRIPTION</span></span>
<span data-ttu-id="2f06d-107">Polecenie cmdlet **Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2f06d-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="2f06d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f06d-108">EXAMPLES</span></span>

### <span data-ttu-id="2f06d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f06d-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="2f06d-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="2f06d-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2f06d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f06d-111">PARAMETERS</span></span>

### <span data-ttu-id="2f06d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f06d-112">-DefaultProfile</span></span>
<span data-ttu-id="2f06d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f06d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f06d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f06d-114">-Name</span></span>
<span data-ttu-id="2f06d-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="2f06d-115">WebApp Name</span></span>

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

### <span data-ttu-id="2f06d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f06d-116">-ResourceGroupName</span></span>
<span data-ttu-id="2f06d-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2f06d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2f06d-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f06d-118">-Slot</span></span>
<span data-ttu-id="2f06d-119">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="2f06d-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2f06d-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="2f06d-120">-WebApp</span></span>
<span data-ttu-id="2f06d-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="2f06d-121">WebApp Object</span></span>

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

### <span data-ttu-id="2f06d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f06d-122">CommonParameters</span></span>
<span data-ttu-id="2f06d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f06d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f06d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f06d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f06d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f06d-125">INPUTS</span></span>

### <span data-ttu-id="2f06d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2f06d-126">System.String</span></span>

### <span data-ttu-id="2f06d-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="2f06d-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f06d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f06d-128">OUTPUTS</span></span>

### <span data-ttu-id="2f06d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2f06d-129">System.String</span></span>

## <span data-ttu-id="2f06d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f06d-130">NOTES</span></span>

## <span data-ttu-id="2f06d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f06d-131">RELATED LINKS</span></span>
