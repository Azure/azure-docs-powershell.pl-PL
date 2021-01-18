---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502551"
---
# <span data-ttu-id="01bb1-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="01bb1-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="01bb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="01bb1-103">Ponowne uruchamianie wystąpienia serwera usług Analysis Services w obecnie zarejestrowanego środowisku zgodnie z opisem w Add-AzAnalysisServicesAccount polecenia</span><span class="sxs-lookup"><span data-stu-id="01bb1-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="01bb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01bb1-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="01bb1-106">Polecenie cmdlet Restart-AzAnalysisServicesInstance powoduje ponowne uruchomienie wystąpienia serwera usługi Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="01bb1-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="01bb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="01bb1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01bb1-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="01bb1-109">To polecenie spowoduje ponowne uruchomienie serwera "testserver" w środowisku określonym w poleceniu Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="01bb1-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="01bb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01bb1-110">PARAMETERS</span></span>

### <span data-ttu-id="01bb1-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="01bb1-111">-Instance</span></span>
<span data-ttu-id="01bb1-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="01bb1-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="01bb1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01bb1-113">-PassThru</span></span>
<span data-ttu-id="01bb1-114">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="01bb1-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="01bb1-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01bb1-115">-Confirm</span></span>
<span data-ttu-id="01bb1-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01bb1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bb1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01bb1-117">-WhatIf</span></span>
<span data-ttu-id="01bb1-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01bb1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01bb1-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01bb1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bb1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bb1-120">CommonParameters</span></span>
<span data-ttu-id="01bb1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bb1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bb1-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bb1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bb1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01bb1-123">INPUTS</span></span>

### <span data-ttu-id="01bb1-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="01bb1-124">None</span></span>

## <span data-ttu-id="01bb1-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01bb1-125">OUTPUTS</span></span>

### <span data-ttu-id="01bb1-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01bb1-126">System.Boolean</span></span>

## <span data-ttu-id="01bb1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01bb1-127">NOTES</span></span>
<span data-ttu-id="01bb1-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="01bb1-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="01bb1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01bb1-129">RELATED LINKS</span></span>
