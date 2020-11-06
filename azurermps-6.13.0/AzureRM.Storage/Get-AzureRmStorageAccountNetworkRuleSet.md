---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544736"
---
# <span data-ttu-id="5ff0e-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ff0e-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="5ff0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ff0e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff0e-103">Pobieranie właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ff0e-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff0e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ff0e-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ff0e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ff0e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff0e-106">Polecenie cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** Pobiera właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ff0e-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="5ff0e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ff0e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff0e-108">Przykład 1: pobieranie właściwości NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ff0e-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="5ff0e-109">To polecenie pobiera właściwość NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ff0e-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="5ff0e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ff0e-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff0e-111">-DefaultProfile</span></span>
<span data-ttu-id="5ff0e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff0e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff0e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ff0e-113">-Name</span></span>
<span data-ttu-id="5ff0e-114">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ff0e-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff0e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff0e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ff0e-116">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ff0e-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="5ff0e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff0e-117">CommonParameters</span></span>
<span data-ttu-id="5ff0e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff0e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff0e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff0e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff0e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff0e-120">INPUTS</span></span>

### <span data-ttu-id="5ff0e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff0e-121">System.String</span></span>

## <span data-ttu-id="5ff0e-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ff0e-122">OUTPUTS</span></span>

### <span data-ttu-id="5ff0e-123">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ff0e-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="5ff0e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ff0e-124">NOTES</span></span>

## <span data-ttu-id="5ff0e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ff0e-125">RELATED LINKS</span></span>
