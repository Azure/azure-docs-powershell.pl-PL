---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326060"
---
# <span data-ttu-id="1564d-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1564d-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="1564d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1564d-102">SYNOPSIS</span></span>

## <span data-ttu-id="1564d-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1564d-103">SYNTAX</span></span>

### <span data-ttu-id="1564d-104">S1</span><span class="sxs-lookup"><span data-stu-id="1564d-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1564d-105">S2</span><span class="sxs-lookup"><span data-stu-id="1564d-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1564d-106">Opis</span><span class="sxs-lookup"><span data-stu-id="1564d-106">DESCRIPTION</span></span>
<span data-ttu-id="1564d-107">Polecenie cmdlet **Reset-AzWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1564d-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="1564d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1564d-108">EXAMPLES</span></span>

### <span data-ttu-id="1564d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1564d-109">Example 1</span></span>

<span data-ttu-id="1564d-110">Poniższy przykład resetuje profil publikowania dla aplikacji sieci Web IpRule skojarzonej z grupą zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="1564d-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="1564d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1564d-111">PARAMETERS</span></span>

### <span data-ttu-id="1564d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1564d-112">-DefaultProfile</span></span>
<span data-ttu-id="1564d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1564d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1564d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1564d-114">-Name</span></span>
<span data-ttu-id="1564d-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1564d-115">WebApp Name</span></span>

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

### <span data-ttu-id="1564d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1564d-116">-ResourceGroupName</span></span>
<span data-ttu-id="1564d-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1564d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="1564d-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1564d-118">-WebApp</span></span>
<span data-ttu-id="1564d-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1564d-119">WebApp Object</span></span>

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

### <span data-ttu-id="1564d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1564d-120">CommonParameters</span></span>
<span data-ttu-id="1564d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1564d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1564d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1564d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1564d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1564d-123">INPUTS</span></span>

### <span data-ttu-id="1564d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1564d-124">System.String</span></span>

### <span data-ttu-id="1564d-125">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="1564d-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1564d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1564d-126">OUTPUTS</span></span>

### <span data-ttu-id="1564d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1564d-127">System.String</span></span>

## <span data-ttu-id="1564d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1564d-128">NOTES</span></span>

## <span data-ttu-id="1564d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1564d-129">RELATED LINKS</span></span>
