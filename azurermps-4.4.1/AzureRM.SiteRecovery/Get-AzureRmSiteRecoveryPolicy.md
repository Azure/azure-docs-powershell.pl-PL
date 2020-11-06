---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 443abbab086fe08ac0a667776a07c792115aa5dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552339"
---
# <span data-ttu-id="188a1-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="188a1-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="188a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="188a1-102">SYNOPSIS</span></span>
<span data-ttu-id="188a1-103">Pobiera zasady ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="188a1-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="188a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="188a1-104">SYNTAX</span></span>

### <span data-ttu-id="188a1-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="188a1-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="188a1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="188a1-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="188a1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="188a1-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="188a1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="188a1-108">DESCRIPTION</span></span>
<span data-ttu-id="188a1-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryPolicy** pobiera listę skonfigurowanych zasad ochrony usługi Azure Site Recovery lub określonych zasad ochrony według nazwy.</span><span class="sxs-lookup"><span data-stu-id="188a1-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="188a1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="188a1-110">EXAMPLES</span></span>

## <span data-ttu-id="188a1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="188a1-111">PARAMETERS</span></span>

### <span data-ttu-id="188a1-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="188a1-112">-FriendlyName</span></span>
<span data-ttu-id="188a1-113">Określa przyjazną nazwę zasad replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="188a1-113">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188a1-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="188a1-114">-Name</span></span>
<span data-ttu-id="188a1-115">Określa nazwę zasad replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="188a1-115">Specifies the name of the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188a1-116">-DefaultProfile</span></span>
<span data-ttu-id="188a1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="188a1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="188a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188a1-118">CommonParameters</span></span>
<span data-ttu-id="188a1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188a1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188a1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="188a1-121">INPUTS</span></span>

## <span data-ttu-id="188a1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="188a1-122">OUTPUTS</span></span>

### <span data-ttu-id="188a1-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="188a1-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="188a1-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="188a1-124">NOTES</span></span>

## <span data-ttu-id="188a1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="188a1-125">RELATED LINKS</span></span>

[<span data-ttu-id="188a1-126">Nowe — AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="188a1-126">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="188a1-127">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="188a1-127">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
