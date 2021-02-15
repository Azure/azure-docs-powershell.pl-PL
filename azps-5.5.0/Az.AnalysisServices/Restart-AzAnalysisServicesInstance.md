---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182402"
---
# <span data-ttu-id="d693f-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="d693f-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="d693f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d693f-102">SYNOPSIS</span></span>
<span data-ttu-id="d693f-103">Ponowne uruchamianie wystąpienia serwera usług Analysis Services w obecnie zalogowanym środowisku zgodnie z Add-AzAnalysisServicesAccount programu</span><span class="sxs-lookup"><span data-stu-id="d693f-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d693f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d693f-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d693f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d693f-105">DESCRIPTION</span></span>
<span data-ttu-id="d693f-106">Polecenie Restart-AzAnalysisServicesInstance powoduje ponowne uruchomienie wystąpienia serwera usług Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d693f-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="d693f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d693f-107">EXAMPLES</span></span>

### <span data-ttu-id="d693f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d693f-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="d693f-109">To polecenie spowoduje ponowne uruchomienie serwera "serwer testowy" w środowisku określonym przez Add-AzAnalysisServicesAccount serwera</span><span class="sxs-lookup"><span data-stu-id="d693f-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d693f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d693f-110">PARAMETERS</span></span>

### <span data-ttu-id="d693f-111">—Instance</span><span class="sxs-lookup"><span data-stu-id="d693f-111">-Instance</span></span>
<span data-ttu-id="d693f-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="d693f-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="d693f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d693f-113">-PassThru</span></span>
<span data-ttu-id="d693f-114">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="d693f-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d693f-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d693f-115">-Confirm</span></span>
<span data-ttu-id="d693f-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d693f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d693f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d693f-117">-WhatIf</span></span>
<span data-ttu-id="d693f-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d693f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d693f-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d693f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d693f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d693f-120">CommonParameters</span></span>
<span data-ttu-id="d693f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d693f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d693f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d693f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d693f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d693f-123">INPUTS</span></span>

### <span data-ttu-id="d693f-124">Brak</span><span class="sxs-lookup"><span data-stu-id="d693f-124">None</span></span>

## <span data-ttu-id="d693f-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d693f-125">OUTPUTS</span></span>

### <span data-ttu-id="d693f-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d693f-126">System.Boolean</span></span>

## <span data-ttu-id="d693f-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d693f-127">NOTES</span></span>
<span data-ttu-id="d693f-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="d693f-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="d693f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d693f-129">RELATED LINKS</span></span>
