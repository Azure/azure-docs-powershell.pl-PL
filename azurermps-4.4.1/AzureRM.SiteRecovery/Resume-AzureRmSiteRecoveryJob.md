---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717780"
---
# <span data-ttu-id="c5761-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c5761-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="c5761-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5761-102">SYNOPSIS</span></span>
<span data-ttu-id="c5761-103">Wznawia wstrzymane zadanie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="c5761-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5761-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5761-104">SYNTAX</span></span>

### <span data-ttu-id="c5761-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5761-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5761-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c5761-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5761-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5761-107">DESCRIPTION</span></span>
<span data-ttu-id="c5761-108">Polecenie cmdlet **Resume-AzureRmSiteRecoveryJob** Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c5761-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="c5761-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5761-109">EXAMPLES</span></span>

## <span data-ttu-id="c5761-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5761-110">PARAMETERS</span></span>

### <span data-ttu-id="c5761-111">-Komentarze</span><span class="sxs-lookup"><span data-stu-id="c5761-111">-Comments</span></span>
<span data-ttu-id="c5761-112">Określa komentarze dotyczące dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="c5761-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5761-113">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="c5761-113">-Job</span></span>
<span data-ttu-id="c5761-114">Określa obiekt zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="c5761-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="c5761-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5761-115">-Name</span></span>
<span data-ttu-id="c5761-116">Określa unikatową nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="c5761-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="c5761-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5761-117">-DefaultProfile</span></span>
<span data-ttu-id="c5761-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5761-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5761-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5761-119">CommonParameters</span></span>
<span data-ttu-id="c5761-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5761-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5761-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5761-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5761-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5761-122">INPUTS</span></span>

### <span data-ttu-id="c5761-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="c5761-123">ASRJob</span></span>
<span data-ttu-id="c5761-124">Parametr "zadanie" akceptuje wartość typu "ASRJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="c5761-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="c5761-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5761-125">OUTPUTS</span></span>

### <span data-ttu-id="c5761-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c5761-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c5761-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5761-127">NOTES</span></span>

## <span data-ttu-id="c5761-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5761-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5761-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c5761-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="c5761-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c5761-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="c5761-131">Zatrzymaj — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c5761-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
