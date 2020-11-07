---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708224"
---
# <span data-ttu-id="25f5a-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="25f5a-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="25f5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="25f5a-103">Pobiera zaawansowaną zasadę ochrony przed zagrożeniami dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="25f5a-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="25f5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25f5a-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25f5a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="25f5a-106">`Get-AzSecurityAdvancedThreatProtection`Polecenie cmdlet pobiera zasady ochrony przed zagrożeniami dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="25f5a-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="25f5a-107">Aby użyć tego polecenia cmdlet, określ parametr *ResourceID* .</span><span class="sxs-lookup"><span data-stu-id="25f5a-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="25f5a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25f5a-108">EXAMPLES</span></span>

### <span data-ttu-id="25f5a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25f5a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="25f5a-110">To polecenie uzyskuje zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="25f5a-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="25f5a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25f5a-111">PARAMETERS</span></span>

### <span data-ttu-id="25f5a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f5a-112">-DefaultProfile</span></span>
<span data-ttu-id="25f5a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25f5a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25f5a-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25f5a-114">-ResourceId</span></span>
<span data-ttu-id="25f5a-115">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="25f5a-115">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f5a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f5a-116">CommonParameters</span></span>
<span data-ttu-id="25f5a-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f5a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f5a-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f5a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f5a-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25f5a-119">INPUTS</span></span>

### <span data-ttu-id="25f5a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="25f5a-120">System.String</span></span>

## <span data-ttu-id="25f5a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25f5a-121">OUTPUTS</span></span>

### <span data-ttu-id="25f5a-122">Microsoft. Azure. Commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="25f5a-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="25f5a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25f5a-123">NOTES</span></span>

## <span data-ttu-id="25f5a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25f5a-124">RELATED LINKS</span></span>
