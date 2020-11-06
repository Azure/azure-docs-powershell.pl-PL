---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553791"
---
# <span data-ttu-id="13945-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="13945-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="13945-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13945-102">SYNOPSIS</span></span>
<span data-ttu-id="13945-103">Pobiera zasady replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="13945-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13945-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13945-104">SYNTAX</span></span>

### <span data-ttu-id="13945-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="13945-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="13945-106">ByName</span><span class="sxs-lookup"><span data-stu-id="13945-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="13945-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="13945-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="13945-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13945-108">DESCRIPTION</span></span>
<span data-ttu-id="13945-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** pobiera listę skonfigurowanych zasad replikacji usługi Azure Site Recovery lub określonych zasad replikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="13945-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="13945-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13945-110">EXAMPLES</span></span>

### <span data-ttu-id="13945-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13945-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="13945-112">Retruns zasady replikacji o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="13945-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="13945-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13945-113">PARAMETERS</span></span>

### <span data-ttu-id="13945-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="13945-114">-FriendlyName</span></span>
<span data-ttu-id="13945-115">Określa przyjazną nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="13945-115">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13945-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13945-116">-Name</span></span>
<span data-ttu-id="13945-117">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="13945-117">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13945-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13945-118">CommonParameters</span></span>
<span data-ttu-id="13945-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13945-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13945-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13945-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13945-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13945-121">INPUTS</span></span>

### <span data-ttu-id="13945-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13945-122">None</span></span>

## <span data-ttu-id="13945-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13945-123">OUTPUTS</span></span>

### <span data-ttu-id="13945-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13945-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13945-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13945-125">NOTES</span></span>

## <span data-ttu-id="13945-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13945-126">RELATED LINKS</span></span>

[<span data-ttu-id="13945-127">Nowe — AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="13945-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="13945-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="13945-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
