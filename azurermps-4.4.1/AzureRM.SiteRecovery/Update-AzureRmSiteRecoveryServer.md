---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549824"
---
# <span data-ttu-id="401a0-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="401a0-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="401a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="401a0-102">SYNOPSIS</span></span>
<span data-ttu-id="401a0-103">Odświeża serwer odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="401a0-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="401a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="401a0-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="401a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="401a0-105">DESCRIPTION</span></span>
<span data-ttu-id="401a0-106">Polecenie cmdlet **Update-AzureRmSiteRecoveryServer** odświeża serwer odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="401a0-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="401a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="401a0-107">EXAMPLES</span></span>

## <span data-ttu-id="401a0-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="401a0-108">PARAMETERS</span></span>

### <span data-ttu-id="401a0-109">-Server</span><span class="sxs-lookup"><span data-stu-id="401a0-109">-Server</span></span>
<span data-ttu-id="401a0-110">Określa serwer odzyskiwania witryny, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="401a0-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="401a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401a0-111">-DefaultProfile</span></span>
<span data-ttu-id="401a0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="401a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="401a0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401a0-113">CommonParameters</span></span>
<span data-ttu-id="401a0-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401a0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401a0-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401a0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401a0-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="401a0-116">INPUTS</span></span>

### <span data-ttu-id="401a0-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="401a0-117">ASRServer</span></span>
<span data-ttu-id="401a0-118">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="401a0-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="401a0-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="401a0-119">OUTPUTS</span></span>

## <span data-ttu-id="401a0-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="401a0-120">NOTES</span></span>

## <span data-ttu-id="401a0-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="401a0-121">RELATED LINKS</span></span>

[<span data-ttu-id="401a0-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="401a0-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="401a0-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="401a0-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
