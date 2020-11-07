---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718086"
---
# <span data-ttu-id="56989-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56989-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="56989-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56989-102">SYNOPSIS</span></span>
<span data-ttu-id="56989-103">Pobiera magazyny odzyskiwania witryny z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56989-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56989-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56989-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56989-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56989-105">DESCRIPTION</span></span>
<span data-ttu-id="56989-106">Polecenie cmdlet **Get-AzureRmSiteRecoveryVault** pobiera listę magazynów odzyskiwania witryny usługi Azure lub określonego magazynu do odtworzenia witryny z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56989-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="56989-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56989-107">EXAMPLES</span></span>

## <span data-ttu-id="56989-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56989-108">PARAMETERS</span></span>

### <span data-ttu-id="56989-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56989-109">-Name</span></span>
<span data-ttu-id="56989-110">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="56989-110">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="56989-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56989-111">-ResourceGroupName</span></span>
<span data-ttu-id="56989-112">Określa nazwę grupy zasobów platformy Azure, z której ma zostać wyświetlony obiekt usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="56989-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

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

### <span data-ttu-id="56989-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56989-113">-DefaultProfile</span></span>
<span data-ttu-id="56989-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56989-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56989-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56989-115">CommonParameters</span></span>
<span data-ttu-id="56989-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56989-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56989-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56989-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56989-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56989-118">INPUTS</span></span>

## <span data-ttu-id="56989-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56989-119">OUTPUTS</span></span>

### <span data-ttu-id="56989-120">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="56989-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="56989-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56989-121">NOTES</span></span>

## <span data-ttu-id="56989-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56989-122">RELATED LINKS</span></span>

[<span data-ttu-id="56989-123">Nowe — AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56989-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="56989-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56989-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
