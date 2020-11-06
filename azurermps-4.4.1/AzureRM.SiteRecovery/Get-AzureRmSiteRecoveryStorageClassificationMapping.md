---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552328"
---
# <span data-ttu-id="3e90a-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3e90a-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="3e90a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e90a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e90a-103">Pobiera mapowanie klasyfikacji magazynu w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="3e90a-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e90a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e90a-104">SYNTAX</span></span>

### <span data-ttu-id="3e90a-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3e90a-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e90a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3e90a-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e90a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e90a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e90a-108">Polecenie cmdlet **Get-AzureRmSiteRecoveryStorageClassificationMapping** pobiera mapowanie klasyfikacji magazynu w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3e90a-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="3e90a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e90a-109">EXAMPLES</span></span>

## <span data-ttu-id="3e90a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e90a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e90a-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e90a-111">-Name</span></span>
<span data-ttu-id="3e90a-112">Określa nazwę mapowania klasyfikacji magazynu, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e90a-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3e90a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e90a-113">-DefaultProfile</span></span>
<span data-ttu-id="3e90a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e90a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e90a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e90a-115">CommonParameters</span></span>
<span data-ttu-id="3e90a-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e90a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e90a-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e90a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e90a-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e90a-118">INPUTS</span></span>

## <span data-ttu-id="3e90a-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e90a-119">OUTPUTS</span></span>

### <span data-ttu-id="3e90a-120">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="3e90a-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="3e90a-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e90a-121">NOTES</span></span>

## <span data-ttu-id="3e90a-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e90a-122">RELATED LINKS</span></span>

[<span data-ttu-id="3e90a-123">Nowe — AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3e90a-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="3e90a-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3e90a-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
