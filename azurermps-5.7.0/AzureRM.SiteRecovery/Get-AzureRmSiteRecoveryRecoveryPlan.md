---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718451"
---
# <span data-ttu-id="4c7ac-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c7ac-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4c7ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7ac-103">Pobiera plan odzyskiwania w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c7ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c7ac-104">SYNTAX</span></span>

### <span data-ttu-id="4c7ac-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4c7ac-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ac-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4c7ac-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ac-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c7ac-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c7ac-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4c7ac-108">DESCRIPTION</span></span>
<span data-ttu-id="4c7ac-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryRecoveryPlan** pobiera plan odzyskiwania w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="4c7ac-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c7ac-110">EXAMPLES</span></span>

## <span data-ttu-id="4c7ac-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c7ac-111">PARAMETERS</span></span>

### <span data-ttu-id="4c7ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7ac-112">-DefaultProfile</span></span>
<span data-ttu-id="4c7ac-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c7ac-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c7ac-114">-FriendlyName</span></span>
<span data-ttu-id="4c7ac-115">Określa przyjazną nazwę planu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ac-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c7ac-116">-Name</span></span>
<span data-ttu-id="4c7ac-117">Określa nazwę planu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ac-118">-Path</span><span class="sxs-lookup"><span data-stu-id="4c7ac-118">-Path</span></span>
<span data-ttu-id="4c7ac-119">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7ac-120">CommonParameters</span></span>
<span data-ttu-id="4c7ac-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7ac-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c7ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7ac-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c7ac-123">INPUTS</span></span>

### <span data-ttu-id="4c7ac-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4c7ac-124">None</span></span>
<span data-ttu-id="4c7ac-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c7ac-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c7ac-126">OUTPUTS</span></span>

### <span data-ttu-id="4c7ac-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="4c7ac-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="4c7ac-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c7ac-128">NOTES</span></span>

## <span data-ttu-id="4c7ac-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c7ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="4c7ac-130">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c7ac-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4c7ac-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c7ac-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4c7ac-132">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c7ac-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
