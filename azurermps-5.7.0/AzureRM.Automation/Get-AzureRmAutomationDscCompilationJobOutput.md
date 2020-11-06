---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: e7093f04cfd7b51f00dcc5cbcd6ad3cb98f54bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554312"
---
# <span data-ttu-id="7a8a9-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7a8a9-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="7a8a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8a9-103">Pobiera strumienie rejestrowania zadania kompilacji DSC usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a8a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a8a9-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a8a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a8a9-105">DESCRIPTION</span></span>
<span data-ttu-id="7a8a9-106">Polecenie cmdlet **Get-AzureRmAutomationDscCompilationJobOutput** pobiera rekordy strumieniowe zadania kompilacji DSC (żądana konfiguracja stanu) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="7a8a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a8a9-107">EXAMPLES</span></span>

### <span data-ttu-id="7a8a9-108">Przykład 1. Pobierz dzienniki zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="7a8a9-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="7a8a9-109">Pierwsze polecenie pobiera zadania kompilacji na koncie usługi Automation o nazwie Contoso17 przy użyciu polecenia cmdlet Get-AzureRmAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="7a8a9-110">Polecenie zapisuje te obiekty w zmiennej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="7a8a9-111">Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="7a8a9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a8a9-112">PARAMETERS</span></span>

### <span data-ttu-id="7a8a9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a8a9-113">-AutomationAccountName</span></span>
<span data-ttu-id="7a8a9-114">Określa nazwę konta automatyzacji zawierającego zadanie kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="7a8a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8a9-115">-DefaultProfile</span></span>
<span data-ttu-id="7a8a9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a8a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a8a9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7a8a9-117">-Id</span></span>
<span data-ttu-id="7a8a9-118">Określa unikatowy identyfikator zadania kompilacji DSC, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a8a9-120">Określa nazwę grupy zasobów zawierającej zadanie kompilacji DSC, dla którego to polecenie cmdlet pobiera rekordy strumieniowe.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="7a8a9-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7a8a9-121">-StartTime</span></span>
<span data-ttu-id="7a8a9-122">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-122">Specifies a start time.</span></span>
<span data-ttu-id="7a8a9-123">To polecenie cmdlet pobiera rekordy strumieniowe, które zadanie kompilacji DSC jest wyprowadzane po upływie tego czasu.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8a9-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="7a8a9-124">-Stream</span></span>
<span data-ttu-id="7a8a9-125">Określa typ strumienia danych wyjściowych, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="7a8a9-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7a8a9-126">Valid values are:</span></span> 

- <span data-ttu-id="7a8a9-127">Jakieś</span><span class="sxs-lookup"><span data-stu-id="7a8a9-127">Any</span></span> 
- <span data-ttu-id="7a8a9-128">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="7a8a9-128">Warning</span></span> 
- <span data-ttu-id="7a8a9-129">Błędów</span><span class="sxs-lookup"><span data-stu-id="7a8a9-129">Error</span></span> 
- <span data-ttu-id="7a8a9-130">Pełne</span><span class="sxs-lookup"><span data-stu-id="7a8a9-130">Verbose</span></span>

```yaml
Type: CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8a9-131">CommonParameters</span></span>
<span data-ttu-id="7a8a9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8a9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8a9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8a9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a8a9-134">INPUTS</span></span>

### <span data-ttu-id="7a8a9-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a8a9-135">None</span></span>
<span data-ttu-id="7a8a9-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a8a9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a8a9-137">OUTPUTS</span></span>

### <span data-ttu-id="7a8a9-138">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="7a8a9-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="7a8a9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a8a9-139">NOTES</span></span>

## <span data-ttu-id="7a8a9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a8a9-140">RELATED LINKS</span></span>

[<span data-ttu-id="7a8a9-141">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7a8a9-141">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="7a8a9-142">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7a8a9-142">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


