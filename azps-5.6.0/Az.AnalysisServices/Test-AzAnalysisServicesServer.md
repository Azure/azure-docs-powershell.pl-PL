---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: cb6680276359fddcf9a98cde3e90cb44185c4e85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959210"
---
# <span data-ttu-id="45d2f-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="45d2f-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="45d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="45d2f-103">Sprawdza istnienie wystąpienia serwera usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="45d2f-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="45d2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45d2f-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45d2f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="45d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="45d2f-106">Polecenie Test-AzAnalysisServicesServer sprawdza istnienie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="45d2f-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="45d2f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45d2f-107">EXAMPLES</span></span>

### <span data-ttu-id="45d2f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45d2f-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="45d2f-109">To polecenie zostanie przetestowane, jeśli w grupie testowej grupy zasobów znajduje się serwer o nazwie serwer testowy</span><span class="sxs-lookup"><span data-stu-id="45d2f-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="45d2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45d2f-110">PARAMETERS</span></span>

### <span data-ttu-id="45d2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d2f-111">-DefaultProfile</span></span>
<span data-ttu-id="45d2f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45d2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d2f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="45d2f-113">-Name</span></span>
<span data-ttu-id="45d2f-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="45d2f-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="45d2f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d2f-115">-ResourceGroupName</span></span>
<span data-ttu-id="45d2f-116">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="45d2f-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="45d2f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d2f-117">CommonParameters</span></span>
<span data-ttu-id="45d2f-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d2f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d2f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d2f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d2f-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45d2f-120">INPUTS</span></span>

### <span data-ttu-id="45d2f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="45d2f-121">System.String</span></span>

## <span data-ttu-id="45d2f-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45d2f-122">OUTPUTS</span></span>

### <span data-ttu-id="45d2f-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45d2f-123">System.Boolean</span></span>

## <span data-ttu-id="45d2f-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45d2f-124">NOTES</span></span>
<span data-ttu-id="45d2f-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="45d2f-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="45d2f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45d2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="45d2f-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="45d2f-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="45d2f-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="45d2f-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
