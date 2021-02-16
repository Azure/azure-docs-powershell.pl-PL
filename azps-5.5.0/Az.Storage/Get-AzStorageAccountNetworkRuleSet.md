---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201330"
---
# <span data-ttu-id="befb1-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="befb1-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="befb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befb1-102">SYNOPSIS</span></span>
<span data-ttu-id="befb1-103">Uzyskiwanie właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="befb1-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="befb1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="befb1-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="befb1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="befb1-105">DESCRIPTION</span></span>
<span data-ttu-id="befb1-106">Polecenie **cmdlet Get-AzStorageAccountNetworkRuleSet** pobiera właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="befb1-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="befb1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="befb1-107">EXAMPLES</span></span>

### <span data-ttu-id="befb1-108">Przykład 1. Uzyskiwanie właściwości NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="befb1-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="befb1-109">To polecenie pobiera właściwość NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="befb1-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="befb1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="befb1-110">PARAMETERS</span></span>

### <span data-ttu-id="befb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befb1-111">-DefaultProfile</span></span>
<span data-ttu-id="befb1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="befb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="befb1-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="befb1-113">-Name</span></span>
<span data-ttu-id="befb1-114">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="befb1-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="befb1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befb1-115">-ResourceGroupName</span></span>
<span data-ttu-id="befb1-116">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="befb1-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="befb1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befb1-117">CommonParameters</span></span>
<span data-ttu-id="befb1-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="befb1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befb1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="befb1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befb1-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="befb1-120">INPUTS</span></span>

### <span data-ttu-id="befb1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="befb1-121">System.String</span></span>

## <span data-ttu-id="befb1-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="befb1-122">OUTPUTS</span></span>

### <span data-ttu-id="befb1-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="befb1-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="befb1-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="befb1-124">NOTES</span></span>

## <span data-ttu-id="befb1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="befb1-125">RELATED LINKS</span></span>
