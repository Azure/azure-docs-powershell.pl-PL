---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345622"
---
# <span data-ttu-id="2d766-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d766-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2d766-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d766-102">SYNOPSIS</span></span>
<span data-ttu-id="2d766-103">Testowanie istnienia wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2d766-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="2d766-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d766-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d766-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d766-105">DESCRIPTION</span></span>
<span data-ttu-id="2d766-106">Polecenie cmdlet Test-AzAnalysisServicesServer sprawdza istnienie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2d766-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="2d766-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d766-107">EXAMPLES</span></span>

### <span data-ttu-id="2d766-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d766-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2d766-109">To polecenie zostanie przetestowane, jeśli w ramach testera zasobów znajduje się serwer o nazwie TestServer</span><span class="sxs-lookup"><span data-stu-id="2d766-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2d766-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d766-110">PARAMETERS</span></span>

### <span data-ttu-id="2d766-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d766-111">-DefaultProfile</span></span>
<span data-ttu-id="2d766-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d766-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d766-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d766-113">-Name</span></span>
<span data-ttu-id="2d766-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2d766-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2d766-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d766-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d766-116">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="2d766-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2d766-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d766-117">CommonParameters</span></span>
<span data-ttu-id="2d766-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d766-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d766-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d766-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d766-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d766-120">INPUTS</span></span>

### <span data-ttu-id="2d766-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2d766-121">System.String</span></span>

## <span data-ttu-id="2d766-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d766-122">OUTPUTS</span></span>

### <span data-ttu-id="2d766-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d766-123">System.Boolean</span></span>

## <span data-ttu-id="2d766-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d766-124">NOTES</span></span>
<span data-ttu-id="2d766-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="2d766-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="2d766-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d766-126">RELATED LINKS</span></span>

[<span data-ttu-id="2d766-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d766-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2d766-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d766-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
