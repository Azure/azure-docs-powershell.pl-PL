---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 038c7456f849777f16ca0113d799b4ee8a16cd2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525818"
---
# <span data-ttu-id="133cb-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="133cb-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="133cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="133cb-102">SYNOPSIS</span></span>
<span data-ttu-id="133cb-103">Ponowne uruchamianie wystąpienia serwera usług Analysis Services w obecnie zarejestrowanego środowisku zgodnie z opisem w Add-AzureAnalysisServicesAccount polecenia</span><span class="sxs-lookup"><span data-stu-id="133cb-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="133cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="133cb-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="133cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="133cb-105">DESCRIPTION</span></span>
<span data-ttu-id="133cb-106">Polecenie cmdlet Restart-AzureAnalysisServicesInstance powoduje ponowne uruchomienie wystąpienia serwera usługi Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="133cb-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="133cb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="133cb-107">EXAMPLES</span></span>

### <span data-ttu-id="133cb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="133cb-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="133cb-109">To polecenie spowoduje ponowne uruchomienie serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="133cb-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="133cb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="133cb-110">PARAMETERS</span></span>

### <span data-ttu-id="133cb-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="133cb-111">-Instance</span></span>
<span data-ttu-id="133cb-112">Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="133cb-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133cb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="133cb-113">-PassThru</span></span>
<span data-ttu-id="133cb-114">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="133cb-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="133cb-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="133cb-115">-Confirm</span></span>
<span data-ttu-id="133cb-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="133cb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133cb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133cb-117">-WhatIf</span></span>
<span data-ttu-id="133cb-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="133cb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133cb-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="133cb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133cb-120">CommonParameters</span></span>
<span data-ttu-id="133cb-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133cb-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133cb-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="133cb-123">INPUTS</span></span>

## <span data-ttu-id="133cb-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="133cb-124">OUTPUTS</span></span>

### <span data-ttu-id="133cb-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="133cb-125">System.Boolean</span></span>

## <span data-ttu-id="133cb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="133cb-126">NOTES</span></span>
<span data-ttu-id="133cb-127">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="133cb-127">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="133cb-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="133cb-128">RELATED LINKS</span></span>

