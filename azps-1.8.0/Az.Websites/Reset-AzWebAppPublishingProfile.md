---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81eaa3b287a14cdc9aa71150c2f0b3724aeb4f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707279"
---
# <span data-ttu-id="f5cb3-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f5cb3-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f5cb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5cb3-102">SYNOPSIS</span></span>

## <span data-ttu-id="f5cb3-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5cb3-103">SYNTAX</span></span>

### <span data-ttu-id="f5cb3-104">S1</span><span class="sxs-lookup"><span data-stu-id="f5cb3-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5cb3-105">S2</span><span class="sxs-lookup"><span data-stu-id="f5cb3-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5cb3-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f5cb3-106">DESCRIPTION</span></span>
<span data-ttu-id="f5cb3-107">Polecenie cmdlet **Reset-AzWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f5cb3-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="f5cb3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5cb3-108">EXAMPLES</span></span>

### <span data-ttu-id="f5cb3-109">1:1</span><span class="sxs-lookup"><span data-stu-id="f5cb3-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f5cb3-110">To polecenie resetuje profil publikowania dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="f5cb3-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f5cb3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5cb3-111">PARAMETERS</span></span>

### <span data-ttu-id="f5cb3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cb3-112">-DefaultProfile</span></span>
<span data-ttu-id="f5cb3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5cb3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5cb3-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5cb3-114">-Name</span></span>
<span data-ttu-id="f5cb3-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5cb3-115">WebApp Name</span></span>

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

### <span data-ttu-id="f5cb3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cb3-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5cb3-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5cb3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f5cb3-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5cb3-118">-WebApp</span></span>
<span data-ttu-id="f5cb3-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5cb3-119">WebApp Object</span></span>

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

### <span data-ttu-id="f5cb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cb3-120">CommonParameters</span></span>
<span data-ttu-id="f5cb3-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5cb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cb3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5cb3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cb3-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5cb3-123">INPUTS</span></span>

### <span data-ttu-id="f5cb3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f5cb3-124">System.String</span></span>

### <span data-ttu-id="f5cb3-125">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="f5cb3-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5cb3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5cb3-126">OUTPUTS</span></span>

### <span data-ttu-id="f5cb3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f5cb3-127">System.String</span></span>

## <span data-ttu-id="f5cb3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5cb3-128">NOTES</span></span>

## <span data-ttu-id="f5cb3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5cb3-129">RELATED LINKS</span></span>
