---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500442"
---
# <span data-ttu-id="51388-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="51388-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="51388-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51388-102">SYNOPSIS</span></span>
<span data-ttu-id="51388-103">Pobiera szczegóły serwera usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="51388-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="51388-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51388-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51388-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51388-105">DESCRIPTION</span></span>
<span data-ttu-id="51388-106">Polecenie cmdlet Get-AzAnalysisServicesServer powoduje wyświetlenie szczegółów dotyczących serwera usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="51388-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="51388-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51388-107">EXAMPLES</span></span>

### <span data-ttu-id="51388-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51388-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="51388-109">To polecenie pobiera wszystkie serwery usługi Azure Analysis Services w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="51388-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="51388-110">Przykład 2: uzyskiwanie serwera</span><span class="sxs-lookup"><span data-stu-id="51388-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="51388-111">To polecenie pobiera serwer usług Azure Analysis Services o nazwie TestServer w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="51388-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="51388-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51388-112">PARAMETERS</span></span>

### <span data-ttu-id="51388-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51388-113">-DefaultProfile</span></span>
<span data-ttu-id="51388-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51388-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51388-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51388-115">-Name</span></span>
<span data-ttu-id="51388-116">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="51388-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="51388-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51388-117">-ResourceGroupName</span></span>
<span data-ttu-id="51388-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="51388-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="51388-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51388-119">CommonParameters</span></span>
<span data-ttu-id="51388-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51388-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51388-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51388-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51388-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51388-122">INPUTS</span></span>

### <span data-ttu-id="51388-123">System. String</span><span class="sxs-lookup"><span data-stu-id="51388-123">System.String</span></span>

## <span data-ttu-id="51388-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51388-124">OUTPUTS</span></span>

### <span data-ttu-id="51388-125">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="51388-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="51388-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51388-126">NOTES</span></span>
<span data-ttu-id="51388-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="51388-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="51388-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51388-128">RELATED LINKS</span></span>

[<span data-ttu-id="51388-129">Nowe — AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="51388-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="51388-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="51388-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
