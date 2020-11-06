---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528166"
---
# <span data-ttu-id="eeaa4-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="eeaa4-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="eeaa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eeaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaa4-103">Eksportuje dziennik z wystąpienia serwera usług Analysis Services w aktualnie zarejestrowanym środowisku, określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeaa4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eeaa4-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="eeaa4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eeaa4-105">DESCRIPTION</span></span>
<span data-ttu-id="eeaa4-106">Polecenie cmdlet Export-AzureAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usługi Azure Analysis Services do pliku</span><span class="sxs-lookup"><span data-stu-id="eeaa4-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="eeaa4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eeaa4-107">EXAMPLES</span></span>

### <span data-ttu-id="eeaa4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eeaa4-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="eeaa4-109">To polecenie spowoduje wyeksportowanie dziennika z serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount i zapisanie go w pliku określonym w OutputPath "C:\path\to\log\testserver.log".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="eeaa4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eeaa4-110">PARAMETERS</span></span>

### <span data-ttu-id="eeaa4-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="eeaa4-111">-Instance</span></span>
<span data-ttu-id="eeaa4-112">Nazwa wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="eeaa4-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa4-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="eeaa4-113">-OutputPath</span></span>
<span data-ttu-id="eeaa4-114">Ścieżka wyjściowa do pliku w celu wyeksportowania dziennika</span><span class="sxs-lookup"><span data-stu-id="eeaa4-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaa4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eeaa4-115">-Force</span></span>
<span data-ttu-id="eeaa4-116">Zastąp plik, jeśli istnieje, bez pytania</span><span class="sxs-lookup"><span data-stu-id="eeaa4-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="eeaa4-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eeaa4-117">INPUTS</span></span>

### <span data-ttu-id="eeaa4-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eeaa4-118">None</span></span>
<span data-ttu-id="eeaa4-119">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eeaa4-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eeaa4-120">OUTPUTS</span></span>

## <span data-ttu-id="eeaa4-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eeaa4-121">NOTES</span></span>
<span data-ttu-id="eeaa4-122">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="eeaa4-122">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="eeaa4-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eeaa4-123">RELATED LINKS</span></span>

