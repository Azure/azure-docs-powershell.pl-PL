---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054182"
---
# <span data-ttu-id="532db-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="532db-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="532db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="532db-102">SYNOPSIS</span></span>
<span data-ttu-id="532db-103">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="532db-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="532db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="532db-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="532db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="532db-105">DESCRIPTION</span></span>
<span data-ttu-id="532db-106">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="532db-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="532db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="532db-107">EXAMPLES</span></span>

### <span data-ttu-id="532db-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="532db-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="532db-109">Wyświetlanie listy wszystkich obiektów przydziałów dla magazynu obiektów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="532db-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="532db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="532db-110">PARAMETERS</span></span>

### <span data-ttu-id="532db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532db-111">-DefaultProfile</span></span>
<span data-ttu-id="532db-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="532db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="532db-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="532db-113">-Location</span></span>
<span data-ttu-id="532db-114">Lokalizacja przydziału.</span><span class="sxs-lookup"><span data-stu-id="532db-114">The location of the quota.</span></span>

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

### <span data-ttu-id="532db-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="532db-115">-SubscriptionId</span></span>
<span data-ttu-id="532db-116">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="532db-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="532db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532db-117">CommonParameters</span></span>
<span data-ttu-id="532db-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="532db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532db-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="532db-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532db-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="532db-120">INPUTS</span></span>

## <span data-ttu-id="532db-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="532db-121">OUTPUTS</span></span>

### <span data-ttu-id="532db-122">Microsoft. Azure. PowerShell. polecenia. KeyVaultAdmin. models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="532db-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="532db-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="532db-123">NOTES</span></span>

## <span data-ttu-id="532db-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="532db-124">RELATED LINKS</span></span>

