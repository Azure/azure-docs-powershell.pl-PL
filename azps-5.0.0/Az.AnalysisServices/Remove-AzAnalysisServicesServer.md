---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225447"
---
# <span data-ttu-id="8f3bd-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8f3bd-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8f3bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3bd-103">Usuwanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8f3bd-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="8f3bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f3bd-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f3bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f3bd-105">DESCRIPTION</span></span>
<span data-ttu-id="8f3bd-106">Polecenie cmdlet Remove-AzAnalysisServicesServer powoduje usunięcie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8f3bd-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="8f3bd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f3bd-107">EXAMPLES</span></span>

### <span data-ttu-id="8f3bd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f3bd-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="8f3bd-109">To polecenie usunie serwer o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="8f3bd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f3bd-110">PARAMETERS</span></span>

### <span data-ttu-id="8f3bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3bd-111">-DefaultProfile</span></span>
<span data-ttu-id="8f3bd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f3bd-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f3bd-113">-Name</span></span>
<span data-ttu-id="8f3bd-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8f3bd-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8f3bd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f3bd-115">-PassThru</span></span>
<span data-ttu-id="8f3bd-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="8f3bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f3bd-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="8f3bd-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8f3bd-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f3bd-119">-Confirm</span></span>
<span data-ttu-id="8f3bd-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8f3bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3bd-121">-WhatIf</span></span>
<span data-ttu-id="8f3bd-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8f3bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3bd-123">CommonParameters</span></span>
<span data-ttu-id="8f3bd-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f3bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3bd-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3bd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3bd-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f3bd-126">INPUTS</span></span>

### <span data-ttu-id="8f3bd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8f3bd-127">System.String</span></span>

## <span data-ttu-id="8f3bd-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f3bd-128">OUTPUTS</span></span>

### <span data-ttu-id="8f3bd-129">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8f3bd-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8f3bd-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f3bd-130">NOTES</span></span>
<span data-ttu-id="8f3bd-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="8f3bd-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="8f3bd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f3bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f3bd-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8f3bd-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="8f3bd-134">Nowe — AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8f3bd-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
