---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545847"
---
# <span data-ttu-id="9ea6e-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="9ea6e-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="9ea6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ea6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea6e-103">Ponowne uruchamianie wystąpienia serwera usług Analysis Services w obecnie zarejestrowanego środowisku zgodnie z opisem w Add-AzureAnalysisServicesAccount polecenia</span><span class="sxs-lookup"><span data-stu-id="9ea6e-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ea6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ea6e-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9ea6e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ea6e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea6e-106">Polecenie cmdlet Restart-AzureAnalysisServicesInstance powoduje ponowne uruchomienie wystąpienia serwera usługi Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9ea6e-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="9ea6e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ea6e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea6e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ea6e-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="9ea6e-109">To polecenie spowoduje ponowne uruchomienie serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9ea6e-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="9ea6e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ea6e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea6e-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="9ea6e-111">-Instance</span></span>
<span data-ttu-id="9ea6e-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="9ea6e-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="9ea6e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ea6e-113">-PassThru</span></span>
<span data-ttu-id="9ea6e-114">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="9ea6e-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9ea6e-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ea6e-115">-Confirm</span></span>
<span data-ttu-id="9ea6e-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea6e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea6e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea6e-117">-WhatIf</span></span>
<span data-ttu-id="9ea6e-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea6e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea6e-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ea6e-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="9ea6e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ea6e-120">INPUTS</span></span>

### <span data-ttu-id="9ea6e-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9ea6e-121">None</span></span>
<span data-ttu-id="9ea6e-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9ea6e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ea6e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ea6e-123">OUTPUTS</span></span>

### <span data-ttu-id="9ea6e-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ea6e-124">System.Boolean</span></span>

## <span data-ttu-id="9ea6e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ea6e-125">NOTES</span></span>
<span data-ttu-id="9ea6e-126">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="9ea6e-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="9ea6e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ea6e-127">RELATED LINKS</span></span>

