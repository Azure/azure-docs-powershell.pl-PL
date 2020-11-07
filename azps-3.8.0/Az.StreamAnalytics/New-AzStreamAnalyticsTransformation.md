---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 833ad7d57259d9a1f308c676ba49a93935d7e045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894318"
---
# <span data-ttu-id="20a05-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="20a05-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="20a05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20a05-102">SYNOPSIS</span></span>
<span data-ttu-id="20a05-103">Umożliwia utworzenie lub zaktualizowanie transformacji w ramach zadania.</span><span class="sxs-lookup"><span data-stu-id="20a05-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="20a05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20a05-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20a05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20a05-105">DESCRIPTION</span></span>
<span data-ttu-id="20a05-106">Polecenie cmdlet **New-AzStreamAnalyticsTransformation** tworzy transformację w ramach zadania Stream Analytics lub aktualizuje istniejące przekształcenie.</span><span class="sxs-lookup"><span data-stu-id="20a05-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="20a05-107">Nazwę przekształcenia można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="20a05-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="20a05-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="20a05-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="20a05-109">Jeśli określisz już istniejącą transformację i nie określisz parametru Force, zostanie wyświetlony monit z pytaniem o to, czy zamienić istniejące przekształcenie.</span><span class="sxs-lookup"><span data-stu-id="20a05-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="20a05-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę przekształcenia, transformacja zostanie zastąpiona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="20a05-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="20a05-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20a05-111">EXAMPLES</span></span>

### <span data-ttu-id="20a05-112">PRZYKŁAD 1. Tworzenie lub zamienianie przekształcenia w zadaniu</span><span class="sxs-lookup"><span data-stu-id="20a05-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="20a05-113">To polecenie tworzy transformację o nazwie StreamingJobTransform w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="20a05-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="20a05-114">Jeśli istniejące przekształcenie jest już zdefiniowane w tej nazwie, zostanie wyświetlony monit z pytaniem, czy chcesz go zamienić.</span><span class="sxs-lookup"><span data-stu-id="20a05-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="20a05-115">PRZYKŁAD 2: zamiana transformacji w zadaniu</span><span class="sxs-lookup"><span data-stu-id="20a05-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="20a05-116">To polecenie zamienia definicję StreamingJobTransform w StreamingJob zadania bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="20a05-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="20a05-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20a05-117">PARAMETERS</span></span>

### <span data-ttu-id="20a05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a05-118">-DefaultProfile</span></span>
<span data-ttu-id="20a05-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20a05-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a05-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="20a05-120">-File</span></span>
<span data-ttu-id="20a05-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON transformacji usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="20a05-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a05-122">-Force</span><span class="sxs-lookup"><span data-stu-id="20a05-122">-Force</span></span>
<span data-ttu-id="20a05-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="20a05-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a05-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="20a05-124">-JobName</span></span>
<span data-ttu-id="20a05-125">Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć transformację analizy strumienia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20a05-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="20a05-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20a05-126">-Name</span></span>
<span data-ttu-id="20a05-127">Określa nazwę przekształcenia usługi Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="20a05-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a05-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a05-128">-ResourceGroupName</span></span>
<span data-ttu-id="20a05-129">Określa nazwę grupy zasobów, w której ma zostać utworzone przekształcanie analizy strumienia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20a05-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="20a05-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20a05-130">-Confirm</span></span>
<span data-ttu-id="20a05-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a05-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a05-132">-WhatIf</span></span>
<span data-ttu-id="20a05-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a05-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20a05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a05-135">CommonParameters</span></span>
<span data-ttu-id="20a05-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a05-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a05-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a05-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20a05-138">INPUTS</span></span>

### <span data-ttu-id="20a05-139">System. String</span><span class="sxs-lookup"><span data-stu-id="20a05-139">System.String</span></span>

## <span data-ttu-id="20a05-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20a05-140">OUTPUTS</span></span>

### <span data-ttu-id="20a05-141">Microsoft. Azure. Commands. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="20a05-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="20a05-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20a05-142">NOTES</span></span>

## <span data-ttu-id="20a05-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20a05-143">RELATED LINKS</span></span>

[<span data-ttu-id="20a05-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="20a05-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


