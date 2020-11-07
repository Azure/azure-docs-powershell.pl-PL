---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: ad827cece73c4ad3add34312befc2f9ae99ca984
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707134"
---
# <span data-ttu-id="6409a-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="6409a-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="6409a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6409a-102">SYNOPSIS</span></span>
<span data-ttu-id="6409a-103">Eksportuje dziennik z wystąpienia serwera usług Analysis Services w aktualnie zarejestrowanym środowisku, określonym w Add-AzAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="6409a-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="6409a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6409a-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6409a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6409a-105">DESCRIPTION</span></span>
<span data-ttu-id="6409a-106">Polecenie cmdlet Export-AzAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usługi Azure Analysis Services do pliku</span><span class="sxs-lookup"><span data-stu-id="6409a-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="6409a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6409a-107">EXAMPLES</span></span>

### <span data-ttu-id="6409a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6409a-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="6409a-109">To polecenie spowoduje wyeksportowanie dziennika z serwera "testserver" w środowisku określonym w poleceniu Add-AzAnalysisServicesAccount i zapisanie go w pliku określonym w OutputPath "C:\path\to\log\testserver.log".</span><span class="sxs-lookup"><span data-stu-id="6409a-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="6409a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6409a-110">PARAMETERS</span></span>

### <span data-ttu-id="6409a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6409a-111">-Force</span></span>
<span data-ttu-id="6409a-112">Zastąp plik, jeśli istnieje, bez pytania</span><span class="sxs-lookup"><span data-stu-id="6409a-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="6409a-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="6409a-113">-Instance</span></span>
<span data-ttu-id="6409a-114">Nazwa wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6409a-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="6409a-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="6409a-115">-OutputPath</span></span>
<span data-ttu-id="6409a-116">Ścieżka wyjściowa do pliku w celu wyeksportowania dziennika</span><span class="sxs-lookup"><span data-stu-id="6409a-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="6409a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6409a-117">-PassThru</span></span>
<span data-ttu-id="6409a-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6409a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6409a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6409a-119">-Confirm</span></span>
<span data-ttu-id="6409a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6409a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6409a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6409a-121">-WhatIf</span></span>
<span data-ttu-id="6409a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6409a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6409a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6409a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6409a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6409a-124">CommonParameters</span></span>
<span data-ttu-id="6409a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6409a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6409a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6409a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6409a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6409a-127">INPUTS</span></span>

### <span data-ttu-id="6409a-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6409a-128">None</span></span>

## <span data-ttu-id="6409a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6409a-129">OUTPUTS</span></span>

### <span data-ttu-id="6409a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="6409a-130">System.Void</span></span>

## <span data-ttu-id="6409a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6409a-131">NOTES</span></span>
<span data-ttu-id="6409a-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="6409a-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="6409a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6409a-133">RELATED LINKS</span></span>
