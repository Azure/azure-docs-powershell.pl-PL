---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192571"
---
# <span data-ttu-id="41490-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="41490-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="41490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41490-102">SYNOPSIS</span></span>
<span data-ttu-id="41490-103">Zawiesza wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="41490-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="41490-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41490-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41490-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="41490-105">DESCRIPTION</span></span>
<span data-ttu-id="41490-106">Polecenie Suspend-AzAnalysisServicesServer zawiesza wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="41490-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="41490-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41490-107">EXAMPLES</span></span>

### <span data-ttu-id="41490-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41490-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="41490-109">To polecenie spowoduje zawieszenie aktywnego serwera o nazwie serwer testowy w grupie testowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41490-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="41490-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41490-110">PARAMETERS</span></span>

### <span data-ttu-id="41490-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41490-111">-DefaultProfile</span></span>
<span data-ttu-id="41490-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41490-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41490-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41490-113">-Name</span></span>
<span data-ttu-id="41490-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="41490-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="41490-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41490-115">-PassThru</span></span>
<span data-ttu-id="41490-116">Jeśli operacja zostanie pomyślnie ukończona, zostaną zwrócone szczegóły usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="41490-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="41490-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41490-117">-ResourceGroupName</span></span>
<span data-ttu-id="41490-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="41490-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41490-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41490-119">-Confirm</span></span>
<span data-ttu-id="41490-120">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="41490-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="41490-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41490-121">-WhatIf</span></span>
<span data-ttu-id="41490-122">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="41490-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="41490-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41490-123">CommonParameters</span></span>
<span data-ttu-id="41490-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41490-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41490-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41490-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41490-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41490-126">INPUTS</span></span>

### <span data-ttu-id="41490-127">System.String</span><span class="sxs-lookup"><span data-stu-id="41490-127">System.String</span></span>

## <span data-ttu-id="41490-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41490-128">OUTPUTS</span></span>

### <span data-ttu-id="41490-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="41490-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="41490-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41490-130">NOTES</span></span>
<span data-ttu-id="41490-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="41490-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="41490-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41490-132">RELATED LINKS</span></span>

[<span data-ttu-id="41490-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="41490-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="41490-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="41490-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

