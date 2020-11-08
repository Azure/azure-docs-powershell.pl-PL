---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233305"
---
# <span data-ttu-id="db2b2-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="db2b2-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="db2b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="db2b2-103">Tworzenie konfiguracji strefy DNS dla prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="db2b2-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="db2b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db2b2-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db2b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="db2b2-106">Polecenie cmdlet **New-AzPrivateDnsZoneConfig** umożliwia utworzenie nowego obiektu konfiguracji strefy DNS, który będzie ustawiony w grupie strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="db2b2-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="db2b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db2b2-107">EXAMPLES</span></span>

### <span data-ttu-id="db2b2-108">Tworzenie konfiguracji strefy DNS</span><span class="sxs-lookup"><span data-stu-id="db2b2-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="db2b2-109">W powyższym przykładzie przedstawiono tworzenie strefy DNS, a następnie Tworzenie konfiguracji strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="db2b2-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="db2b2-110">`New-AzPrivateDnsZone` polecenie cmdlet jest provededne przez moduł AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="db2b2-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="db2b2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db2b2-111">PARAMETERS</span></span>

### <span data-ttu-id="db2b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2b2-112">-DefaultProfile</span></span>
<span data-ttu-id="db2b2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db2b2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db2b2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db2b2-114">-Name</span></span>
<span data-ttu-id="db2b2-115">Nazwa zasobu, który jest unikatowy w obrębie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db2b2-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="db2b2-116">Ta nazwa może być używana do uzyskiwania dostępu do zasobu.</span><span class="sxs-lookup"><span data-stu-id="db2b2-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="db2b2-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="db2b2-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="db2b2-118">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="db2b2-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="db2b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2b2-119">CommonParameters</span></span>
<span data-ttu-id="db2b2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2b2-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db2b2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2b2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db2b2-122">INPUTS</span></span>

### <span data-ttu-id="db2b2-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="db2b2-123">None</span></span>

## <span data-ttu-id="db2b2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db2b2-124">OUTPUTS</span></span>

### <span data-ttu-id="db2b2-125">Microsoft. Azure. Commands. Network. models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="db2b2-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="db2b2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db2b2-126">NOTES</span></span>

## <span data-ttu-id="db2b2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db2b2-127">RELATED LINKS</span></span>
