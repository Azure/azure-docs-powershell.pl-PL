---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 7f47d800fd0eab51edae321f9d21260f50075b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543995"
---
# <span data-ttu-id="98a91-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="98a91-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="98a91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98a91-102">SYNOPSIS</span></span>
<span data-ttu-id="98a91-103">Testowanie istnienia wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="98a91-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98a91-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98a91-105">DESCRIPTION</span></span>
<span data-ttu-id="98a91-106">Polecenie cmdlet Test-AzureRmAnalysisServicesServer sprawdza istnienie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="98a91-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="98a91-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98a91-107">EXAMPLES</span></span>

### <span data-ttu-id="98a91-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98a91-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="98a91-109">To polecenie zostanie przetestowane, jeśli w ramach testera zasobów znajduje się serwer o nazwie TestServer</span><span class="sxs-lookup"><span data-stu-id="98a91-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="98a91-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98a91-110">PARAMETERS</span></span>

### <span data-ttu-id="98a91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a91-111">-DefaultProfile</span></span>
<span data-ttu-id="98a91-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98a91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a91-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98a91-113">-Name</span></span>
<span data-ttu-id="98a91-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="98a91-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="98a91-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a91-115">-ResourceGroupName</span></span>
<span data-ttu-id="98a91-116">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="98a91-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="98a91-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a91-117">CommonParameters</span></span>
<span data-ttu-id="98a91-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a91-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a91-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a91-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a91-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98a91-120">INPUTS</span></span>

### <span data-ttu-id="98a91-121">System. String</span><span class="sxs-lookup"><span data-stu-id="98a91-121">System.String</span></span>

## <span data-ttu-id="98a91-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98a91-122">OUTPUTS</span></span>

### <span data-ttu-id="98a91-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98a91-123">System.Boolean</span></span>

## <span data-ttu-id="98a91-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98a91-124">NOTES</span></span>
<span data-ttu-id="98a91-125">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="98a91-125">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="98a91-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98a91-126">RELATED LINKS</span></span>

[<span data-ttu-id="98a91-127">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="98a91-127">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="98a91-128">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="98a91-128">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
