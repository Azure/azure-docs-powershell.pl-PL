---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242875"
---
# <span data-ttu-id="74dd6-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="74dd6-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="74dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74dd6-102">SYNOPSIS</span></span>

## <span data-ttu-id="74dd6-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74dd6-103">SYNTAX</span></span>

### <span data-ttu-id="74dd6-104">S1</span><span class="sxs-lookup"><span data-stu-id="74dd6-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74dd6-105">S2</span><span class="sxs-lookup"><span data-stu-id="74dd6-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74dd6-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="74dd6-106">DESCRIPTION</span></span>
<span data-ttu-id="74dd6-107">Polecenie **cmdlet Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="74dd6-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="74dd6-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74dd6-108">EXAMPLES</span></span>

### <span data-ttu-id="74dd6-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74dd6-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="74dd6-110">To polecenie powoduje zresetowanie profilu publikowania dla typu Slot o nazwie Slot001 dla aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="74dd6-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="74dd6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74dd6-111">PARAMETERS</span></span>

### <span data-ttu-id="74dd6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74dd6-112">-DefaultProfile</span></span>
<span data-ttu-id="74dd6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74dd6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74dd6-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74dd6-114">-Name</span></span>
<span data-ttu-id="74dd6-115">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="74dd6-115">WebApp Name</span></span>

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

### <span data-ttu-id="74dd6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74dd6-116">-ResourceGroupName</span></span>
<span data-ttu-id="74dd6-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="74dd6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="74dd6-118">— Slot</span><span class="sxs-lookup"><span data-stu-id="74dd6-118">-Slot</span></span>
<span data-ttu-id="74dd6-119">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="74dd6-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="74dd6-120">- WebApp</span><span class="sxs-lookup"><span data-stu-id="74dd6-120">-WebApp</span></span>
<span data-ttu-id="74dd6-121">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="74dd6-121">WebApp Object</span></span>

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

### <span data-ttu-id="74dd6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74dd6-122">CommonParameters</span></span>
<span data-ttu-id="74dd6-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74dd6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74dd6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74dd6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74dd6-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74dd6-125">INPUTS</span></span>

### <span data-ttu-id="74dd6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="74dd6-126">System.String</span></span>

### <span data-ttu-id="74dd6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="74dd6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="74dd6-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74dd6-128">OUTPUTS</span></span>

### <span data-ttu-id="74dd6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="74dd6-129">System.String</span></span>

## <span data-ttu-id="74dd6-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74dd6-130">NOTES</span></span>

## <span data-ttu-id="74dd6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74dd6-131">RELATED LINKS</span></span>
