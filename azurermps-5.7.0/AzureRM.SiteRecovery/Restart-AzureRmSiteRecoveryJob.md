---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524901"
---
# <span data-ttu-id="af764-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="af764-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="af764-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af764-102">SYNOPSIS</span></span>
<span data-ttu-id="af764-103">Ponowne uruchamianie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="af764-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af764-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af764-104">SYNTAX</span></span>

### <span data-ttu-id="af764-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af764-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af764-106">ByName</span><span class="sxs-lookup"><span data-stu-id="af764-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af764-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af764-107">DESCRIPTION</span></span>
<span data-ttu-id="af764-108">Polecenie cmdlet **restart-AzureRmSiteRecoveryJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="af764-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="af764-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af764-109">EXAMPLES</span></span>

## <span data-ttu-id="af764-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af764-110">PARAMETERS</span></span>

### <span data-ttu-id="af764-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af764-111">-DefaultProfile</span></span>
<span data-ttu-id="af764-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af764-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af764-113">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="af764-113">-Job</span></span>
<span data-ttu-id="af764-114">Określa obiekt zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="af764-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="af764-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af764-115">-Name</span></span>
<span data-ttu-id="af764-116">Określa unikatową nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="af764-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="af764-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af764-117">CommonParameters</span></span>
<span data-ttu-id="af764-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af764-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af764-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af764-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af764-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af764-120">INPUTS</span></span>

### <span data-ttu-id="af764-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="af764-121">ASRJob</span></span>
<span data-ttu-id="af764-122">Parametr "zadanie" akceptuje wartość typu "ASRJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="af764-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="af764-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af764-123">OUTPUTS</span></span>

### <span data-ttu-id="af764-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af764-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af764-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af764-125">NOTES</span></span>

## <span data-ttu-id="af764-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af764-126">RELATED LINKS</span></span>

[<span data-ttu-id="af764-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="af764-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="af764-128">Życiorys — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="af764-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="af764-129">Zatrzymaj — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="af764-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
