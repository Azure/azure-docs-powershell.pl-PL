---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542092"
---
# <span data-ttu-id="b058b-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b058b-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="b058b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b058b-102">SYNOPSIS</span></span>
<span data-ttu-id="b058b-103">Eksportuje dziennik z wystąpienia serwera usług Analysis Services w aktualnie zarejestrowanym środowisku, określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="b058b-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b058b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b058b-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b058b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b058b-105">DESCRIPTION</span></span>
<span data-ttu-id="b058b-106">Polecenie cmdlet Export-AzureAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usługi Azure Analysis Services do pliku</span><span class="sxs-lookup"><span data-stu-id="b058b-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="b058b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b058b-107">EXAMPLES</span></span>

### <span data-ttu-id="b058b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b058b-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="b058b-109">To polecenie spowoduje wyeksportowanie dziennika z serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount i zapisanie go w pliku określonym w OutputPath "C:\path\to\log\testserver.log".</span><span class="sxs-lookup"><span data-stu-id="b058b-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="b058b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b058b-110">PARAMETERS</span></span>

### <span data-ttu-id="b058b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b058b-111">-Force</span></span>
<span data-ttu-id="b058b-112">Zastąp plik, jeśli istnieje, bez pytania</span><span class="sxs-lookup"><span data-stu-id="b058b-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="b058b-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="b058b-113">-Instance</span></span>
<span data-ttu-id="b058b-114">Nazwa wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b058b-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="b058b-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b058b-115">-OutputPath</span></span>
<span data-ttu-id="b058b-116">Ścieżka wyjściowa do pliku w celu wyeksportowania dziennika</span><span class="sxs-lookup"><span data-stu-id="b058b-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="b058b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b058b-117">-Confirm</span></span>
<span data-ttu-id="b058b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b058b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b058b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b058b-119">-WhatIf</span></span>
<span data-ttu-id="b058b-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b058b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b058b-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b058b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b058b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b058b-122">CommonParameters</span></span>
<span data-ttu-id="b058b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b058b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b058b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b058b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b058b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b058b-125">INPUTS</span></span>

### <span data-ttu-id="b058b-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b058b-126">None</span></span>

## <span data-ttu-id="b058b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b058b-127">OUTPUTS</span></span>

### <span data-ttu-id="b058b-128">System. void</span><span class="sxs-lookup"><span data-stu-id="b058b-128">System.Void</span></span>

## <span data-ttu-id="b058b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b058b-129">NOTES</span></span>
<span data-ttu-id="b058b-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b058b-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="b058b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b058b-131">RELATED LINKS</span></span>
