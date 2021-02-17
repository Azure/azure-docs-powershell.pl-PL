---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184410"
---
# <span data-ttu-id="62acc-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="62acc-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="62acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62acc-102">SYNOPSIS</span></span>
<span data-ttu-id="62acc-103">Tworzy konfigurację strefy DNS prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="62acc-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="62acc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62acc-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62acc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="62acc-105">DESCRIPTION</span></span>
<span data-ttu-id="62acc-106">Polecenie cmdlet **New-AzPrivateDnsZoneConfig** umożliwia utworzenie nowego obiektu konfiguracji strefy DNS, który będzie ustawiony w grupie stref DNS.</span><span class="sxs-lookup"><span data-stu-id="62acc-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="62acc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62acc-107">EXAMPLES</span></span>

### <span data-ttu-id="62acc-108">Tworzy konfigurację strefy DNS</span><span class="sxs-lookup"><span data-stu-id="62acc-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="62acc-109">Powyższy przykład tworzy strefę DNS, a następnie tworzy konfigurację strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="62acc-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="62acc-110">`New-AzPrivateDnsZone` Polecenie cmdlet jest udowodnione przez moduł Az.PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="62acc-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="62acc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62acc-111">PARAMETERS</span></span>

### <span data-ttu-id="62acc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62acc-112">-DefaultProfile</span></span>
<span data-ttu-id="62acc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62acc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62acc-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62acc-114">-Name</span></span>
<span data-ttu-id="62acc-115">Nazwa zasobu unikatowego w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="62acc-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="62acc-116">Za pomocą tej nazwy można uzyskać dostęp do zasobu.</span><span class="sxs-lookup"><span data-stu-id="62acc-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="62acc-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="62acc-118">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="62acc-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62acc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62acc-119">CommonParameters</span></span>
<span data-ttu-id="62acc-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62acc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62acc-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62acc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62acc-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62acc-122">INPUTS</span></span>

### <span data-ttu-id="62acc-123">Brak</span><span class="sxs-lookup"><span data-stu-id="62acc-123">None</span></span>

## <span data-ttu-id="62acc-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62acc-124">OUTPUTS</span></span>

### <span data-ttu-id="62acc-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="62acc-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="62acc-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62acc-126">NOTES</span></span>

## <span data-ttu-id="62acc-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62acc-127">RELATED LINKS</span></span>
