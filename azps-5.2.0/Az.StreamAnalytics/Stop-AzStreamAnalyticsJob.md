---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366256"
---
# <span data-ttu-id="86b15-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="86b15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86b15-102">SYNOPSIS</span></span>
<span data-ttu-id="86b15-103">Zatrzymuje zadanie analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="86b15-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="86b15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86b15-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86b15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86b15-105">DESCRIPTION</span></span>
<span data-ttu-id="86b15-106">Polecenie cmdlet **stop-AzStreamAnalyticsJob** asynchronicznie zatrzymuje działanie funkcji Stream Analytics na platformie Azure i derezerwuje zasoby, które były używane.</span><span class="sxs-lookup"><span data-stu-id="86b15-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="86b15-107">Definicja zadania i metadane pozostają dostępne w ramach abonamentu za pośrednictwem interfejsów API portalu i zarządzania Azure, takich jak zadanie można edytować i ponownie uruchomić.</span><span class="sxs-lookup"><span data-stu-id="86b15-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="86b15-108">Nie zostanie naliczona opłata za zadanie w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="86b15-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="86b15-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86b15-109">EXAMPLES</span></span>

### <span data-ttu-id="86b15-110">Przykład 1: Zatrzymywanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="86b15-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="86b15-111">To polecenie zatrzymuje zadanie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="86b15-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="86b15-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86b15-112">PARAMETERS</span></span>

### <span data-ttu-id="86b15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b15-113">-DefaultProfile</span></span>
<span data-ttu-id="86b15-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86b15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86b15-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86b15-115">-Name</span></span>
<span data-ttu-id="86b15-116">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="86b15-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b15-117">-ResourceGroupName</span></span>
<span data-ttu-id="86b15-118">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="86b15-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b15-119">CommonParameters</span></span>
<span data-ttu-id="86b15-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b15-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b15-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b15-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86b15-122">INPUTS</span></span>

### <span data-ttu-id="86b15-123">System. String</span><span class="sxs-lookup"><span data-stu-id="86b15-123">System.String</span></span>

## <span data-ttu-id="86b15-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86b15-124">OUTPUTS</span></span>

### <span data-ttu-id="86b15-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86b15-125">System.Boolean</span></span>

## <span data-ttu-id="86b15-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86b15-126">NOTES</span></span>

## <span data-ttu-id="86b15-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86b15-127">RELATED LINKS</span></span>

[<span data-ttu-id="86b15-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="86b15-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="86b15-130">Nowe — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="86b15-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="86b15-132">Start — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="86b15-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


