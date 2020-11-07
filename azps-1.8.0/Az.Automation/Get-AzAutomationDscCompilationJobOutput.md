---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 7a39d010759228e15dd5aee36788f9373ab879bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710598"
---
# <span data-ttu-id="807cc-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="807cc-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="807cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="807cc-102">SYNOPSIS</span></span>
<span data-ttu-id="807cc-103">Pobiera strumienie rejestrowania zadania kompilacji DSC usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="807cc-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="807cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="807cc-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="807cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="807cc-105">DESCRIPTION</span></span>
<span data-ttu-id="807cc-106">Polecenie cmdlet **Get-AzAutomationDscCompilationJobOutput** pobiera rekordy strumieniowe zadania kompilacji DSC (żądana konfiguracja stanu) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="807cc-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="807cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="807cc-107">EXAMPLES</span></span>

### <span data-ttu-id="807cc-108">Przykład 1. Pobierz dzienniki zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="807cc-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="807cc-109">Pierwsze polecenie pobiera zadania kompilacji na koncie usługi Automation o nazwie Contoso17 przy użyciu polecenia cmdlet Get-AzAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="807cc-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="807cc-110">Polecenie zapisuje te obiekty w zmiennej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="807cc-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="807cc-111">Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="807cc-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="807cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="807cc-112">PARAMETERS</span></span>

### <span data-ttu-id="807cc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="807cc-113">-AutomationAccountName</span></span>
<span data-ttu-id="807cc-114">Określa nazwę konta automatyzacji zawierającego zadanie kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="807cc-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="807cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807cc-115">-DefaultProfile</span></span>
<span data-ttu-id="807cc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="807cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="807cc-117">-ID</span><span class="sxs-lookup"><span data-stu-id="807cc-117">-Id</span></span>
<span data-ttu-id="807cc-118">Określa unikatowy identyfikator zadania kompilacji DSC, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="807cc-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="807cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="807cc-120">Określa nazwę grupy zasobów zawierającej zadanie kompilacji DSC, dla którego to polecenie cmdlet pobiera rekordy strumieniowe.</span><span class="sxs-lookup"><span data-stu-id="807cc-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="807cc-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="807cc-121">-StartTime</span></span>
<span data-ttu-id="807cc-122">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="807cc-122">Specifies a start time.</span></span>
<span data-ttu-id="807cc-123">To polecenie cmdlet pobiera rekordy strumieniowe, które zadanie kompilacji DSC jest wyprowadzane po upływie tego czasu.</span><span class="sxs-lookup"><span data-stu-id="807cc-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="807cc-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="807cc-124">-Stream</span></span>
<span data-ttu-id="807cc-125">Określa typ strumienia danych wyjściowych, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="807cc-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="807cc-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="807cc-126">Valid values are:</span></span> 
- <span data-ttu-id="807cc-127">Jakieś</span><span class="sxs-lookup"><span data-stu-id="807cc-127">Any</span></span> 
- <span data-ttu-id="807cc-128">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="807cc-128">Warning</span></span> 
- <span data-ttu-id="807cc-129">Błędów</span><span class="sxs-lookup"><span data-stu-id="807cc-129">Error</span></span> 
- <span data-ttu-id="807cc-130">Pełne</span><span class="sxs-lookup"><span data-stu-id="807cc-130">Verbose</span></span>

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

### <span data-ttu-id="807cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807cc-131">CommonParameters</span></span>
<span data-ttu-id="807cc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807cc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807cc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807cc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="807cc-134">INPUTS</span></span>

### <span data-ttu-id="807cc-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="807cc-135">System.Guid</span></span>

### <span data-ttu-id="807cc-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="807cc-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="807cc-137">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="807cc-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="807cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="807cc-138">System.String</span></span>

## <span data-ttu-id="807cc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="807cc-139">OUTPUTS</span></span>

### <span data-ttu-id="807cc-140">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="807cc-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="807cc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="807cc-141">NOTES</span></span>

## <span data-ttu-id="807cc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="807cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="807cc-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="807cc-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="807cc-144">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="807cc-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


