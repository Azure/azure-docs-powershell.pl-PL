---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f67c22b483b561af8ffcf2ede9bc1e489379c0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717763"
---
# <span data-ttu-id="48ce5-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="48ce5-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="48ce5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="48ce5-103">Pobiera szczegóły serwera usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="48ce5-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48ce5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48ce5-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ce5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="48ce5-106">Polecenie cmdlet Get-AzureRmAnalysisServicesServer powoduje wyświetlenie szczegółów dotyczących serwera usług Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="48ce5-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="48ce5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48ce5-107">EXAMPLES</span></span>

### <span data-ttu-id="48ce5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48ce5-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="48ce5-109">To polecenie pobiera wszystkie serwery usługi Azure Analysis Services w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="48ce5-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="48ce5-110">Przykład 2: uzyskiwanie serwera</span><span class="sxs-lookup"><span data-stu-id="48ce5-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="48ce5-111">To polecenie pobiera serwer usług Azure Analysis Services o nazwie TestServer w grupie zasobów o nazwie ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="48ce5-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="48ce5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48ce5-112">PARAMETERS</span></span>

### <span data-ttu-id="48ce5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ce5-113">-DefaultProfile</span></span>
<span data-ttu-id="48ce5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48ce5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ce5-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48ce5-115">-Name</span></span>
<span data-ttu-id="48ce5-116">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="48ce5-116">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ce5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ce5-117">-ResourceGroupName</span></span>
<span data-ttu-id="48ce5-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="48ce5-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ce5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ce5-119">CommonParameters</span></span>
<span data-ttu-id="48ce5-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ce5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ce5-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ce5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ce5-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ce5-122">INPUTS</span></span>

### <span data-ttu-id="48ce5-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="48ce5-123">None</span></span>
<span data-ttu-id="48ce5-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="48ce5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48ce5-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48ce5-125">OUTPUTS</span></span>

### <span data-ttu-id="48ce5-126">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="48ce5-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="48ce5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48ce5-127">NOTES</span></span>
<span data-ttu-id="48ce5-128">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="48ce5-128">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="48ce5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48ce5-129">RELATED LINKS</span></span>

[<span data-ttu-id="48ce5-130">Nowe — AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="48ce5-130">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="48ce5-131">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="48ce5-131">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
