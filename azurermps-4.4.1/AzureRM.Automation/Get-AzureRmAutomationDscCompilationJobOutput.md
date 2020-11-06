---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: d38971c15c46cbeaba6e9dda87ad0f3b7febbfd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550108"
---
# <span data-ttu-id="500a0-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="500a0-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="500a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="500a0-102">SYNOPSIS</span></span>
<span data-ttu-id="500a0-103">Pobiera strumienie rejestrowania zadania kompilacji DSC usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="500a0-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="500a0-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="500a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="500a0-105">DESCRIPTION</span></span>
<span data-ttu-id="500a0-106">Polecenie cmdlet **Get-AzureRmAutomationDscCompilationJobOutput** pobiera rekordy strumieniowe zadania kompilacji DSC (żądana konfiguracja stanu) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="500a0-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="500a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="500a0-107">EXAMPLES</span></span>

### <span data-ttu-id="500a0-108">Przykład 1. Pobierz dzienniki zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="500a0-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="500a0-109">Pierwsze polecenie pobiera zadania kompilacji na koncie usługi Automation o nazwie Contoso17 przy użyciu polecenia cmdlet Get-AzureRmAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="500a0-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="500a0-110">Polecenie zapisuje te obiekty w zmiennej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="500a0-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="500a0-111">Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="500a0-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="500a0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="500a0-112">PARAMETERS</span></span>

### <span data-ttu-id="500a0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="500a0-113">-AutomationAccountName</span></span>
<span data-ttu-id="500a0-114">Określa nazwę konta automatyzacji zawierającego zadanie kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="500a0-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="500a0-115">-ID</span><span class="sxs-lookup"><span data-stu-id="500a0-115">-Id</span></span>
<span data-ttu-id="500a0-116">Określa unikatowy identyfikator zadania kompilacji DSC, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="500a0-116">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="500a0-118">Określa nazwę grupy zasobów zawierającej zadanie kompilacji DSC, dla którego to polecenie cmdlet pobiera rekordy strumieniowe.</span><span class="sxs-lookup"><span data-stu-id="500a0-118">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="500a0-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="500a0-119">-StartTime</span></span>
<span data-ttu-id="500a0-120">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="500a0-120">Specifies a start time.</span></span>
<span data-ttu-id="500a0-121">To polecenie cmdlet pobiera rekordy strumieniowe, które zadanie kompilacji DSC jest wyprowadzane po upływie tego czasu.</span><span class="sxs-lookup"><span data-stu-id="500a0-121">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500a0-122">-Stream</span><span class="sxs-lookup"><span data-stu-id="500a0-122">-Stream</span></span>
<span data-ttu-id="500a0-123">Określa typ strumienia danych wyjściowych, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500a0-123">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="500a0-124">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="500a0-124">Valid values are:</span></span> 

- <span data-ttu-id="500a0-125">Jakieś</span><span class="sxs-lookup"><span data-stu-id="500a0-125">Any</span></span> 
- <span data-ttu-id="500a0-126">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="500a0-126">Warning</span></span> 
- <span data-ttu-id="500a0-127">Błędów</span><span class="sxs-lookup"><span data-stu-id="500a0-127">Error</span></span> 
- <span data-ttu-id="500a0-128">Pełne</span><span class="sxs-lookup"><span data-stu-id="500a0-128">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500a0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500a0-129">-DefaultProfile</span></span>
<span data-ttu-id="500a0-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="500a0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="500a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500a0-131">CommonParameters</span></span>
<span data-ttu-id="500a0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500a0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500a0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="500a0-134">INPUTS</span></span>

## <span data-ttu-id="500a0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="500a0-135">OUTPUTS</span></span>

### <span data-ttu-id="500a0-136">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="500a0-136">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="500a0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="500a0-137">NOTES</span></span>

## <span data-ttu-id="500a0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="500a0-138">RELATED LINKS</span></span>

[<span data-ttu-id="500a0-139">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="500a0-139">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="500a0-140">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="500a0-140">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


