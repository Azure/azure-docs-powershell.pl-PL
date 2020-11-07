---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891658"
---
# <span data-ttu-id="0f777-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="0f777-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="0f777-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f777-102">SYNOPSIS</span></span>
<span data-ttu-id="0f777-103">Zwraca ustawienia dostawcy zasobów magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f777-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="0f777-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f777-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f777-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f777-105">DESCRIPTION</span></span>
<span data-ttu-id="0f777-106">Zwraca ustawienia dostawcy zasobów magazynu.</span><span class="sxs-lookup"><span data-stu-id="0f777-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="0f777-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f777-107">EXAMPLES</span></span>

### <span data-ttu-id="0f777-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="0f777-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="0f777-109">Pobierz ustawienia miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="0f777-109">Get the storage settings.</span></span>

## <span data-ttu-id="0f777-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f777-110">PARAMETERS</span></span>

### <span data-ttu-id="0f777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f777-111">-DefaultProfile</span></span>
<span data-ttu-id="0f777-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f777-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f777-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0f777-113">-Location</span></span>
<span data-ttu-id="0f777-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0f777-114">Resource location.</span></span>

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

### <span data-ttu-id="0f777-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0f777-115">-SubscriptionId</span></span>
<span data-ttu-id="0f777-116">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="0f777-116">Subscription Id.</span></span>

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

### <span data-ttu-id="0f777-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f777-117">CommonParameters</span></span>
<span data-ttu-id="0f777-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f777-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f777-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f777-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f777-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f777-120">INPUTS</span></span>

## <span data-ttu-id="0f777-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f777-121">OUTPUTS</span></span>

### <span data-ttu-id="0f777-122">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="0f777-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="0f777-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f777-123">NOTES</span></span>

## <span data-ttu-id="0f777-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f777-124">RELATED LINKS</span></span>

