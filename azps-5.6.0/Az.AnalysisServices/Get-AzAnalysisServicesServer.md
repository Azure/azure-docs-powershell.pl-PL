---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: 8c2e7b9fe5335df29308a612ef8a133762e7ab4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015537"
---
# <span data-ttu-id="e7754-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e7754-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="e7754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7754-102">SYNOPSIS</span></span>
<span data-ttu-id="e7754-103">Pobiera szczegółowe informacje o serwerze usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="e7754-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="e7754-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7754-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7754-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7754-105">DESCRIPTION</span></span>
<span data-ttu-id="e7754-106">Polecenie Get-AzAnalysisServicesServer pobiera szczegółowe informacje o serwerze usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="e7754-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="e7754-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7754-107">EXAMPLES</span></span>

### <span data-ttu-id="e7754-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7754-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="e7754-109">To polecenie pobiera wszystkie serwery usług Azure Analysis Services w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="e7754-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="e7754-110">Przykład 2. Uzyskiwanie serwera</span><span class="sxs-lookup"><span data-stu-id="e7754-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="e7754-111">To polecenie pobiera serwer usług Azure Analysis Services o nazwie serwer testowy w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="e7754-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="e7754-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7754-112">PARAMETERS</span></span>

### <span data-ttu-id="e7754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7754-113">-DefaultProfile</span></span>
<span data-ttu-id="e7754-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7754-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7754-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7754-115">-Name</span></span>
<span data-ttu-id="e7754-116">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e7754-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="e7754-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7754-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7754-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="e7754-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7754-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7754-119">CommonParameters</span></span>
<span data-ttu-id="e7754-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7754-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7754-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7754-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7754-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7754-122">INPUTS</span></span>

### <span data-ttu-id="e7754-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e7754-123">System.String</span></span>

## <span data-ttu-id="e7754-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7754-124">OUTPUTS</span></span>

### <span data-ttu-id="e7754-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e7754-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="e7754-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7754-126">NOTES</span></span>
<span data-ttu-id="e7754-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="e7754-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="e7754-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7754-128">RELATED LINKS</span></span>

[<span data-ttu-id="e7754-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="e7754-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="e7754-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="e7754-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
