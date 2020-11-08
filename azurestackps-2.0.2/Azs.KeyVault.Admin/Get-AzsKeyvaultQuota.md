---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061572"
---
# <span data-ttu-id="74cc1-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="74cc1-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="74cc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="74cc1-103">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="74cc1-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="74cc1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74cc1-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="74cc1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="74cc1-106">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="74cc1-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="74cc1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="74cc1-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="74cc1-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="74cc1-109">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="74cc1-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="74cc1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74cc1-110">PARAMETERS</span></span>

### <span data-ttu-id="74cc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cc1-111">-DefaultProfile</span></span>
<span data-ttu-id="74cc1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74cc1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74cc1-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74cc1-113">-Location</span></span>
<span data-ttu-id="74cc1-114">Lokalizacja przydziału.</span><span class="sxs-lookup"><span data-stu-id="74cc1-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74cc1-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="74cc1-115">-SubscriptionId</span></span>
<span data-ttu-id="74cc1-116">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="74cc1-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74cc1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cc1-117">CommonParameters</span></span>
<span data-ttu-id="74cc1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74cc1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cc1-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74cc1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cc1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74cc1-120">INPUTS</span></span>

## <span data-ttu-id="74cc1-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74cc1-121">OUTPUTS</span></span>

### <span data-ttu-id="74cc1-122">Microsoft. Azure. PowerShell. polecenia. KeyVaultAdmin. models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="74cc1-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="74cc1-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74cc1-123">NOTES</span></span>

## <span data-ttu-id="74cc1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74cc1-124">RELATED LINKS</span></span>

