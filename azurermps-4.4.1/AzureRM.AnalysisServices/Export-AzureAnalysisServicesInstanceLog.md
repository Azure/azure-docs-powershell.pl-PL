---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719541"
---
# <span data-ttu-id="f0844-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f0844-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="f0844-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0844-102">SYNOPSIS</span></span>
<span data-ttu-id="f0844-103">Eksportuje dziennik z wystąpienia serwera usług Analysis Services w aktualnie zarejestrowanym środowisku, określonym w Add-AzureAnalysisServicesAccount polecenia.</span><span class="sxs-lookup"><span data-stu-id="f0844-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0844-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0844-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="f0844-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0844-105">DESCRIPTION</span></span>
<span data-ttu-id="f0844-106">Polecenie cmdlet Export-AzureAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usługi Azure Analysis Services do pliku</span><span class="sxs-lookup"><span data-stu-id="f0844-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="f0844-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0844-107">EXAMPLES</span></span>

### <span data-ttu-id="f0844-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0844-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="f0844-109">To polecenie spowoduje wyeksportowanie dziennika z serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount i zapisanie go w pliku określonym w OutputPath "C:\path\to\log\testserver.log".</span><span class="sxs-lookup"><span data-stu-id="f0844-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="f0844-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0844-110">PARAMETERS</span></span>

### <span data-ttu-id="f0844-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="f0844-111">-Instance</span></span>
<span data-ttu-id="f0844-112">Nazwa wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f0844-112">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="f0844-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f0844-113">-OutputPath</span></span>
<span data-ttu-id="f0844-114">Ścieżka wyjściowa do pliku w celu wyeksportowania dziennika</span><span class="sxs-lookup"><span data-stu-id="f0844-114">Output path to file to export log</span></span>

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

### <span data-ttu-id="f0844-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0844-115">-Force</span></span>
<span data-ttu-id="f0844-116">Zastąp plik, jeśli istnieje, bez pytania</span><span class="sxs-lookup"><span data-stu-id="f0844-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="f0844-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0844-117">INPUTS</span></span>

## <span data-ttu-id="f0844-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0844-118">OUTPUTS</span></span>

## <span data-ttu-id="f0844-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0844-119">NOTES</span></span>
<span data-ttu-id="f0844-120">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="f0844-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="f0844-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0844-121">RELATED LINKS</span></span>

