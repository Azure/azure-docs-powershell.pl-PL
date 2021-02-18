---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201203"
---
# <span data-ttu-id="17ed6-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="17ed6-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="17ed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="17ed6-103">Pobiera strumienie rejestrowania zadania kompilacji dsc automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="17ed6-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="17ed6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17ed6-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ed6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="17ed6-106">Polecenie **cmdlet Get-AzAutomationDscCompilationJobOutput** pobiera rekordy strumienia zadania kompilacji APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="17ed6-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="17ed6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="17ed6-108">Przykład 1. Uzyskiwanie dzienników dla zadania kompilacji dsc</span><span class="sxs-lookup"><span data-stu-id="17ed6-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="17ed6-109">Pierwsze polecenie pobiera zadania kompilacji na koncie automatyzacji o nazwie Contoso17 przy użyciu Get-AzAutomationDscCompilationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ed6-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="17ed6-110">Polecenie przechowuje te obiekty w $Jobs zmienną.</span><span class="sxs-lookup"><span data-stu-id="17ed6-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="17ed6-111">Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka $Jobs tablicy.</span><span class="sxs-lookup"><span data-stu-id="17ed6-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="17ed6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17ed6-112">PARAMETERS</span></span>

### <span data-ttu-id="17ed6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17ed6-113">-AutomationAccountName</span></span>
<span data-ttu-id="17ed6-114">Określa nazwę konta automatyzacji zawierającego zadanie kompilacji dsc.</span><span class="sxs-lookup"><span data-stu-id="17ed6-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="17ed6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ed6-115">-DefaultProfile</span></span>
<span data-ttu-id="17ed6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="17ed6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17ed6-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="17ed6-117">-Id</span></span>
<span data-ttu-id="17ed6-118">Określa unikatowy identyfikator zadania kompilacji dsc, dla którego jest wyprowadzone to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ed6-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="17ed6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ed6-119">-ResourceGroupName</span></span>
<span data-ttu-id="17ed6-120">Określa nazwę grupy zasobów zawierającej zadanie kompilacji dsc, dla którego to polecenie cmdlet pobiera rekordy strumienia.</span><span class="sxs-lookup"><span data-stu-id="17ed6-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="17ed6-121">— StartTime</span><span class="sxs-lookup"><span data-stu-id="17ed6-121">-StartTime</span></span>
<span data-ttu-id="17ed6-122">Określa czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="17ed6-122">Specifies a start time.</span></span>
<span data-ttu-id="17ed6-123">To polecenie cmdlet pobiera rekordy strumieniowe, których dane wyjściowe zadania kompilacji dsc są po tym czasie.</span><span class="sxs-lookup"><span data-stu-id="17ed6-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="17ed6-124">— Stream</span><span class="sxs-lookup"><span data-stu-id="17ed6-124">-Stream</span></span>
<span data-ttu-id="17ed6-125">Określa typ strumienia dla wyniku, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ed6-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="17ed6-126">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="17ed6-126">Valid values are:</span></span> 
- <span data-ttu-id="17ed6-127">Dowolna</span><span class="sxs-lookup"><span data-stu-id="17ed6-127">Any</span></span> 
- <span data-ttu-id="17ed6-128">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="17ed6-128">Warning</span></span> 
- <span data-ttu-id="17ed6-129">Błąd</span><span class="sxs-lookup"><span data-stu-id="17ed6-129">Error</span></span> 
- <span data-ttu-id="17ed6-130">Pełne słownictwo</span><span class="sxs-lookup"><span data-stu-id="17ed6-130">Verbose</span></span>

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

### <span data-ttu-id="17ed6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ed6-131">CommonParameters</span></span>
<span data-ttu-id="17ed6-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ed6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ed6-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ed6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ed6-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17ed6-134">INPUTS</span></span>

### <span data-ttu-id="17ed6-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="17ed6-135">System.Guid</span></span>

### <span data-ttu-id="17ed6-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="17ed6-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="17ed6-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17ed6-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17ed6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="17ed6-138">System.String</span></span>

## <span data-ttu-id="17ed6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17ed6-139">OUTPUTS</span></span>

### <span data-ttu-id="17ed6-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="17ed6-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="17ed6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17ed6-141">NOTES</span></span>

## <span data-ttu-id="17ed6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17ed6-142">RELATED LINKS</span></span>

[<span data-ttu-id="17ed6-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="17ed6-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="17ed6-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="17ed6-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


