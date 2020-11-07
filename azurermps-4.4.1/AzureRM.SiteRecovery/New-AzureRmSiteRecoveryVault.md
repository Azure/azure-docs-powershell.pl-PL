---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717154"
---
# <span data-ttu-id="f915f-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f915f-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="f915f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f915f-102">SYNOPSIS</span></span>
<span data-ttu-id="f915f-103">Tworzy magazyn usług odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="f915f-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f915f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f915f-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f915f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f915f-105">DESCRIPTION</span></span>
<span data-ttu-id="f915f-106">Polecenie cmdlet **New-AzureRmSiteRecoveryVault** tworzy magazyn usług Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="f915f-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="f915f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f915f-107">EXAMPLES</span></span>

## <span data-ttu-id="f915f-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f915f-108">PARAMETERS</span></span>

### <span data-ttu-id="f915f-109">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f915f-109">-Location</span></span>
<span data-ttu-id="f915f-110">Określa nazwę lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="f915f-110">Specifies the geographical location name.</span></span>

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

### <span data-ttu-id="f915f-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f915f-111">-Name</span></span>
<span data-ttu-id="f915f-112">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="f915f-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="f915f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f915f-113">-ResourceGroupName</span></span>
<span data-ttu-id="f915f-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f915f-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f915f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f915f-115">-DefaultProfile</span></span>
<span data-ttu-id="f915f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f915f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f915f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f915f-117">CommonParameters</span></span>
<span data-ttu-id="f915f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f915f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f915f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f915f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f915f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f915f-120">INPUTS</span></span>

## <span data-ttu-id="f915f-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f915f-121">OUTPUTS</span></span>

## <span data-ttu-id="f915f-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f915f-122">NOTES</span></span>

## <span data-ttu-id="f915f-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f915f-123">RELATED LINKS</span></span>

[<span data-ttu-id="f915f-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f915f-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="f915f-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f915f-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
