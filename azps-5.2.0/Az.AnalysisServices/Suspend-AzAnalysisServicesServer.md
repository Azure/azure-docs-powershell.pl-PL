---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348829"
---
# <span data-ttu-id="4335f-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4335f-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4335f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4335f-102">SYNOPSIS</span></span>
<span data-ttu-id="4335f-103">Wstrzymuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4335f-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="4335f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4335f-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4335f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4335f-105">DESCRIPTION</span></span>
<span data-ttu-id="4335f-106">Polecenie Suspend-AzAnalysisServicesServer polecenia zawiesza wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4335f-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="4335f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4335f-107">EXAMPLES</span></span>

### <span data-ttu-id="4335f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4335f-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4335f-109">To polecenie spowoduje zawieszenie aktywnego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="4335f-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4335f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4335f-110">PARAMETERS</span></span>

### <span data-ttu-id="4335f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4335f-111">-DefaultProfile</span></span>
<span data-ttu-id="4335f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4335f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4335f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4335f-113">-Name</span></span>
<span data-ttu-id="4335f-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4335f-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4335f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4335f-115">-PassThru</span></span>
<span data-ttu-id="4335f-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="4335f-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="4335f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4335f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4335f-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="4335f-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4335f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4335f-119">-Confirm</span></span>
<span data-ttu-id="4335f-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="4335f-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4335f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4335f-121">-WhatIf</span></span>
<span data-ttu-id="4335f-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="4335f-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4335f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4335f-123">CommonParameters</span></span>
<span data-ttu-id="4335f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4335f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4335f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4335f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4335f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4335f-126">INPUTS</span></span>

### <span data-ttu-id="4335f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4335f-127">System.String</span></span>

## <span data-ttu-id="4335f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4335f-128">OUTPUTS</span></span>

### <span data-ttu-id="4335f-129">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4335f-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4335f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4335f-130">NOTES</span></span>
<span data-ttu-id="4335f-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="4335f-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="4335f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4335f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4335f-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4335f-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4335f-134">Życiorys — AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4335f-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

