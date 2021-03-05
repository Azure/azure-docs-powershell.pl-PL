---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 3e4e3b2c2f90420f198d2900d5de0d519ffde81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015546"
---
# <span data-ttu-id="6db7d-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="6db7d-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="6db7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6db7d-103">Eksportuje dziennik z wystąpienia serwera usług Analysis Services w środowisku obecnie zalogowanym zgodnie z Add-AzAnalysisServicesAccount programu</span><span class="sxs-lookup"><span data-stu-id="6db7d-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="6db7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6db7d-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db7d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6db7d-105">DESCRIPTION</span></span>
<span data-ttu-id="6db7d-106">Polecenie Export-AzAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usług Azure Analysis Services do pliku</span><span class="sxs-lookup"><span data-stu-id="6db7d-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="6db7d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6db7d-107">EXAMPLES</span></span>

### <span data-ttu-id="6db7d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6db7d-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="6db7d-109">To polecenie wyeksportuje dziennik z serwera "serwer testowy" w środowisku określonym za pomocą polecenia Add-AzAnalysisServicesAccount i zapisze go w pliku określonym w pliku outputPath 'C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="6db7d-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="6db7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6db7d-110">PARAMETERS</span></span>

### <span data-ttu-id="6db7d-111">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6db7d-111">-Force</span></span>
<span data-ttu-id="6db7d-112">Zastąp plik, jeśli istnieje bez pytania</span><span class="sxs-lookup"><span data-stu-id="6db7d-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="6db7d-113">—Instance</span><span class="sxs-lookup"><span data-stu-id="6db7d-113">-Instance</span></span>
<span data-ttu-id="6db7d-114">Nazwa wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6db7d-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db7d-115">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="6db7d-115">-OutputPath</span></span>
<span data-ttu-id="6db7d-116">Ścieżka wyjściowa do pliku do wyeksportowania dziennika</span><span class="sxs-lookup"><span data-stu-id="6db7d-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db7d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6db7d-117">-PassThru</span></span>
<span data-ttu-id="6db7d-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6db7d-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6db7d-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6db7d-119">-Confirm</span></span>
<span data-ttu-id="6db7d-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6db7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db7d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db7d-121">-WhatIf</span></span>
<span data-ttu-id="6db7d-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db7d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6db7d-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6db7d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db7d-124">CommonParameters</span></span>
<span data-ttu-id="6db7d-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db7d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db7d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db7d-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db7d-127">INPUTS</span></span>

### <span data-ttu-id="6db7d-128">Brak</span><span class="sxs-lookup"><span data-stu-id="6db7d-128">None</span></span>

## <span data-ttu-id="6db7d-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db7d-129">OUTPUTS</span></span>

### <span data-ttu-id="6db7d-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="6db7d-130">System.Void</span></span>

## <span data-ttu-id="6db7d-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6db7d-131">NOTES</span></span>
<span data-ttu-id="6db7d-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="6db7d-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="6db7d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6db7d-133">RELATED LINKS</span></span>
