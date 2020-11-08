---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051016"
---
# <span data-ttu-id="343c7-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="343c7-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="343c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="343c7-102">SYNOPSIS</span></span>
<span data-ttu-id="343c7-103">Wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="343c7-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="343c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="343c7-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="343c7-105">DESCRIPTION</span></span>
<span data-ttu-id="343c7-106">Polecenie cmdlet Resume-AzAnalysisServicesServer wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="343c7-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="343c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="343c7-107">EXAMPLES</span></span>

### <span data-ttu-id="343c7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="343c7-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="343c7-109">To polecenie spowoduje wznowienie wstrzymanego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="343c7-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="343c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="343c7-110">PARAMETERS</span></span>

### <span data-ttu-id="343c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343c7-111">-DefaultProfile</span></span>
<span data-ttu-id="343c7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="343c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343c7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="343c7-113">-Name</span></span>
<span data-ttu-id="343c7-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="343c7-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="343c7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="343c7-115">-PassThru</span></span>
<span data-ttu-id="343c7-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="343c7-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="343c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="343c7-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="343c7-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="343c7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="343c7-119">-Confirm</span></span>
<span data-ttu-id="343c7-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="343c7-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="343c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343c7-121">-WhatIf</span></span>
<span data-ttu-id="343c7-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="343c7-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="343c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343c7-123">CommonParameters</span></span>
<span data-ttu-id="343c7-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343c7-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343c7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343c7-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="343c7-126">INPUTS</span></span>

### <span data-ttu-id="343c7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="343c7-127">System.String</span></span>

## <span data-ttu-id="343c7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="343c7-128">OUTPUTS</span></span>

### <span data-ttu-id="343c7-129">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="343c7-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="343c7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="343c7-130">NOTES</span></span>
<span data-ttu-id="343c7-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="343c7-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="343c7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="343c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="343c7-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="343c7-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="343c7-134">Suspend — AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="343c7-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
