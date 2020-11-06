---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549836"
---
# <span data-ttu-id="55e6d-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="55e6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="55e6d-103">Ponowne uruchamianie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="55e6d-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55e6d-104">SYNTAX</span></span>

### <span data-ttu-id="55e6d-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55e6d-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e6d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="55e6d-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e6d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55e6d-107">DESCRIPTION</span></span>
<span data-ttu-id="55e6d-108">Polecenie cmdlet **restart-AzureRmSiteRecoveryJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="55e6d-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="55e6d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55e6d-109">EXAMPLES</span></span>

## <span data-ttu-id="55e6d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55e6d-110">PARAMETERS</span></span>

### <span data-ttu-id="55e6d-111">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="55e6d-111">-Job</span></span>
<span data-ttu-id="55e6d-112">Określa obiekt zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="55e6d-112">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55e6d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55e6d-113">-Name</span></span>
<span data-ttu-id="55e6d-114">Określa unikatową nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="55e6d-114">Specifies the unique name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e6d-115">-DefaultProfile</span></span>
<span data-ttu-id="55e6d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55e6d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e6d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e6d-117">CommonParameters</span></span>
<span data-ttu-id="55e6d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e6d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e6d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e6d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e6d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55e6d-120">INPUTS</span></span>

### <span data-ttu-id="55e6d-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-121">ASRJob</span></span>
<span data-ttu-id="55e6d-122">Parametr "zadanie" akceptuje wartość typu "ASRJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="55e6d-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="55e6d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55e6d-123">OUTPUTS</span></span>

### <span data-ttu-id="55e6d-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="55e6d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55e6d-125">NOTES</span></span>

## <span data-ttu-id="55e6d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55e6d-126">RELATED LINKS</span></span>

[<span data-ttu-id="55e6d-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="55e6d-128">Życiorys — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="55e6d-129">Zatrzymaj — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="55e6d-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
