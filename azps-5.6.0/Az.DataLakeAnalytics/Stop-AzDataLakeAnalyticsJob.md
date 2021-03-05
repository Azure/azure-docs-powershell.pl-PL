---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3858c2ad6ca90716d5c9140949a683b9c409a105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015354"
---
# <span data-ttu-id="16c3d-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="16c3d-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="16c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="16c3d-103">Anulowanie zadania.</span><span class="sxs-lookup"><span data-stu-id="16c3d-103">Cancels a job.</span></span>

## <span data-ttu-id="16c3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16c3d-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c3d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="16c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="16c3d-106">Polecenie **cmdlet Stop-AzDataLakeAnalyticsJob** anuluje zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="16c3d-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="16c3d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="16c3d-108">Przykład 1. Anulowanie zadania</span><span class="sxs-lookup"><span data-stu-id="16c3d-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="16c3d-109">To polecenie anuluje zadanie z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="16c3d-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="16c3d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c3d-110">PARAMETERS</span></span>

### <span data-ttu-id="16c3d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="16c3d-111">-Account</span></span>
<span data-ttu-id="16c3d-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="16c3d-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c3d-113">-DefaultProfile</span></span>
<span data-ttu-id="16c3d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="16c3d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16c3d-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="16c3d-115">-Force</span></span>
<span data-ttu-id="16c3d-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="16c3d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-117">- JobId</span><span class="sxs-lookup"><span data-stu-id="16c3d-117">-JobId</span></span>
<span data-ttu-id="16c3d-118">Określa identyfikator zadania do anulowania.</span><span class="sxs-lookup"><span data-stu-id="16c3d-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c3d-119">-PassThru</span></span>
<span data-ttu-id="16c3d-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="16c3d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16c3d-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="16c3d-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16c3d-122">-Confirm</span></span>
<span data-ttu-id="16c3d-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16c3d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c3d-124">-WhatIf</span></span>
<span data-ttu-id="16c3d-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c3d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c3d-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16c3d-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c3d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c3d-127">CommonParameters</span></span>
<span data-ttu-id="16c3d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c3d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c3d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c3d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c3d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16c3d-130">INPUTS</span></span>

### <span data-ttu-id="16c3d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="16c3d-131">System.String</span></span>

### <span data-ttu-id="16c3d-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="16c3d-132">System.Guid</span></span>

### <span data-ttu-id="16c3d-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="16c3d-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16c3d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16c3d-134">OUTPUTS</span></span>

### <span data-ttu-id="16c3d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16c3d-135">System.Boolean</span></span>

## <span data-ttu-id="16c3d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16c3d-136">NOTES</span></span>

## <span data-ttu-id="16c3d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16c3d-137">RELATED LINKS</span></span>

[<span data-ttu-id="16c3d-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="16c3d-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="16c3d-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="16c3d-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="16c3d-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="16c3d-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


