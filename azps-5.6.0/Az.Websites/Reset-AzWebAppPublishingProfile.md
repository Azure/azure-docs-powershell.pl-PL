---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 9d3a17280f80ef0376912f806439698f24cdfe25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008202"
---
# <span data-ttu-id="49e8e-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="49e8e-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="49e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49e8e-102">SYNOPSIS</span></span>

## <span data-ttu-id="49e8e-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49e8e-103">SYNTAX</span></span>

### <span data-ttu-id="49e8e-104">S1</span><span class="sxs-lookup"><span data-stu-id="49e8e-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e8e-105">S2</span><span class="sxs-lookup"><span data-stu-id="49e8e-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e8e-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="49e8e-106">DESCRIPTION</span></span>
<span data-ttu-id="49e8e-107">Polecenie **cmdlet Reset-AzWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="49e8e-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="49e8e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49e8e-108">EXAMPLES</span></span>

### <span data-ttu-id="49e8e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49e8e-109">Example 1</span></span>

<span data-ttu-id="49e8e-110">Poniższy przykład powoduje zresetowanie profilu publikowania dla strony IpRule aplikacji Web App skojarzonej z grupą zasobów MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="49e8e-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="49e8e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49e8e-111">PARAMETERS</span></span>

### <span data-ttu-id="49e8e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e8e-112">-DefaultProfile</span></span>
<span data-ttu-id="49e8e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49e8e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e8e-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49e8e-114">-Name</span></span>
<span data-ttu-id="49e8e-115">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="49e8e-115">WebApp Name</span></span>

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

### <span data-ttu-id="49e8e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e8e-116">-ResourceGroupName</span></span>
<span data-ttu-id="49e8e-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49e8e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="49e8e-118">- WebApp</span><span class="sxs-lookup"><span data-stu-id="49e8e-118">-WebApp</span></span>
<span data-ttu-id="49e8e-119">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="49e8e-119">WebApp Object</span></span>

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

### <span data-ttu-id="49e8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e8e-120">CommonParameters</span></span>
<span data-ttu-id="49e8e-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e8e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e8e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e8e-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e8e-123">INPUTS</span></span>

### <span data-ttu-id="49e8e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="49e8e-124">System.String</span></span>

### <span data-ttu-id="49e8e-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="49e8e-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="49e8e-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e8e-126">OUTPUTS</span></span>

### <span data-ttu-id="49e8e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="49e8e-127">System.String</span></span>

## <span data-ttu-id="49e8e-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49e8e-128">NOTES</span></span>

## <span data-ttu-id="49e8e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49e8e-129">RELATED LINKS</span></span>
