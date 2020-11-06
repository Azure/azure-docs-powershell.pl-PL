---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524790"
---
# <span data-ttu-id="18792-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="18792-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18792-102">SYNOPSIS</span></span>
<span data-ttu-id="18792-103">Zatrzymuje zadanie analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="18792-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18792-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18792-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18792-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18792-105">DESCRIPTION</span></span>
<span data-ttu-id="18792-106">Polecenie cmdlet **stop-AzureRmStreamAnalyticsJob** asynchronicznie zatrzymuje działanie funkcji Stream Analytics na platformie Azure i derezerwuje zasoby, które były używane.</span><span class="sxs-lookup"><span data-stu-id="18792-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="18792-107">Definicja zadania i metadane pozostają dostępne w ramach abonamentu za pośrednictwem interfejsów API portalu i zarządzania Azure, takich jak zadanie można edytować i ponownie uruchomić.</span><span class="sxs-lookup"><span data-stu-id="18792-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="18792-108">Nie zostanie naliczona opłata za zadanie w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="18792-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="18792-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18792-109">EXAMPLES</span></span>

### <span data-ttu-id="18792-110">PRZYKŁAD 1: Zatrzymywanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="18792-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="18792-111">To polecenie zatrzymuje zadanie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="18792-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="18792-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18792-112">PARAMETERS</span></span>

### <span data-ttu-id="18792-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18792-113">-DefaultProfile</span></span>
<span data-ttu-id="18792-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18792-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18792-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18792-115">-Name</span></span>
<span data-ttu-id="18792-116">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="18792-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18792-117">-ResourceGroupName</span></span>
<span data-ttu-id="18792-118">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="18792-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18792-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18792-119">CommonParameters</span></span>
<span data-ttu-id="18792-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18792-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18792-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18792-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18792-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18792-122">INPUTS</span></span>

### <span data-ttu-id="18792-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18792-123">None</span></span>
<span data-ttu-id="18792-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="18792-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18792-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18792-125">OUTPUTS</span></span>

### <span data-ttu-id="18792-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="18792-126">System.Object</span></span>

## <span data-ttu-id="18792-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18792-127">NOTES</span></span>

## <span data-ttu-id="18792-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18792-128">RELATED LINKS</span></span>

[<span data-ttu-id="18792-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="18792-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="18792-131">Nowe — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="18792-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="18792-133">Start — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18792-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


