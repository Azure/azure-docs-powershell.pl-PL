---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891866"
---
# <span data-ttu-id="54cc2-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="54cc2-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="54cc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54cc2-102">SYNOPSIS</span></span>

## <span data-ttu-id="54cc2-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54cc2-103">SYNTAX</span></span>

### <span data-ttu-id="54cc2-104">S1</span><span class="sxs-lookup"><span data-stu-id="54cc2-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54cc2-105">S2</span><span class="sxs-lookup"><span data-stu-id="54cc2-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54cc2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="54cc2-106">DESCRIPTION</span></span>
<span data-ttu-id="54cc2-107">Polecenie cmdlet **Reset-AzWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="54cc2-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="54cc2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54cc2-108">EXAMPLES</span></span>

### <span data-ttu-id="54cc2-109">1:1</span><span class="sxs-lookup"><span data-stu-id="54cc2-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="54cc2-110">To polecenie resetuje profil publikowania dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="54cc2-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="54cc2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54cc2-111">PARAMETERS</span></span>

### <span data-ttu-id="54cc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cc2-112">-DefaultProfile</span></span>
<span data-ttu-id="54cc2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54cc2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54cc2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54cc2-114">-Name</span></span>
<span data-ttu-id="54cc2-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="54cc2-115">WebApp Name</span></span>

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

### <span data-ttu-id="54cc2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cc2-116">-ResourceGroupName</span></span>
<span data-ttu-id="54cc2-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="54cc2-117">Resource Group Name</span></span>

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

### <span data-ttu-id="54cc2-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="54cc2-118">-WebApp</span></span>
<span data-ttu-id="54cc2-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="54cc2-119">WebApp Object</span></span>

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

### <span data-ttu-id="54cc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cc2-120">CommonParameters</span></span>
<span data-ttu-id="54cc2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cc2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cc2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cc2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54cc2-123">INPUTS</span></span>

### <span data-ttu-id="54cc2-124">Klienta</span><span class="sxs-lookup"><span data-stu-id="54cc2-124">Site</span></span>
<span data-ttu-id="54cc2-125">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="54cc2-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="54cc2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54cc2-126">OUTPUTS</span></span>

## <span data-ttu-id="54cc2-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54cc2-127">NOTES</span></span>

## <span data-ttu-id="54cc2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54cc2-128">RELATED LINKS</span></span>

