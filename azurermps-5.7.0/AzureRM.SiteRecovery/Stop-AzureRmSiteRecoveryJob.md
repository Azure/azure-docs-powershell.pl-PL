---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524894"
---
# <span data-ttu-id="d5a53-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="d5a53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5a53-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a53-103">Zatrzymuje zadanie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="d5a53-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5a53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5a53-104">SYNTAX</span></span>

### <span data-ttu-id="d5a53-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d5a53-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a53-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d5a53-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a53-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d5a53-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a53-108">Polecenie cmdlet **stop-AzureRmSiteRecoveryJob** zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a53-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d5a53-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5a53-109">EXAMPLES</span></span>

## <span data-ttu-id="d5a53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5a53-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a53-111">-DefaultProfile</span></span>
<span data-ttu-id="d5a53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a53-113">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d5a53-113">-Job</span></span>
<span data-ttu-id="d5a53-114">Określa obiekt zadania odzyskiwania witryny, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="d5a53-114">Specifies the Site Recovery job object to stop.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a53-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5a53-115">-Name</span></span>
<span data-ttu-id="d5a53-116">Określa unikatową nazwę zadania odzyskiwania witryny, które należy zatrzymać.</span><span class="sxs-lookup"><span data-stu-id="d5a53-116">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="d5a53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a53-117">CommonParameters</span></span>
<span data-ttu-id="d5a53-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a53-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a53-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a53-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a53-120">INPUTS</span></span>

### <span data-ttu-id="d5a53-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-121">ASRJob</span></span>
<span data-ttu-id="d5a53-122">Parametr "zadanie" akceptuje wartość typu "ASRJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="d5a53-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="d5a53-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5a53-123">OUTPUTS</span></span>

### <span data-ttu-id="d5a53-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5a53-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5a53-125">NOTES</span></span>

## <span data-ttu-id="d5a53-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a53-126">RELATED LINKS</span></span>

[<span data-ttu-id="d5a53-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="d5a53-128">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="d5a53-129">Życiorys — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d5a53-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
