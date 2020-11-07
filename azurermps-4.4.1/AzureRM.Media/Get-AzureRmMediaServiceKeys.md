---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719285"
---
# <span data-ttu-id="ada9d-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="ada9d-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="ada9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ada9d-102">SYNOPSIS</span></span>
<span data-ttu-id="ada9d-103">Pobiera kluczowe informacje dotyczące uzyskiwania dostępu do punktu końcowego usługi w usłudze multimediów skojarzonego z usługą Media.</span><span class="sxs-lookup"><span data-stu-id="ada9d-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ada9d-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ada9d-105">DESCRIPTION</span></span>
<span data-ttu-id="ada9d-106">Polecenie cmdlet **Get-AzureRmMediaServiceKeys** pobiera informacje kluczowe o uzyskiwaniu dostępu do punktu końcowego przenoszenia stanu (pozostałej) skojarzonego z usługą Azure Media.</span><span class="sxs-lookup"><span data-stu-id="ada9d-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="ada9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ada9d-107">EXAMPLES</span></span>

### <span data-ttu-id="ada9d-108">Przykład 1: uzyskiwanie najważniejszych informacji dotyczących uzyskiwania dostępu do usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="ada9d-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="ada9d-109">To polecenie pobiera kluczowe informacje dotyczące uzyskiwania dostępu do usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="ada9d-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="ada9d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ada9d-110">PARAMETERS</span></span>

### <span data-ttu-id="ada9d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ada9d-111">-AccountName</span></span>
<span data-ttu-id="ada9d-112">Określa nazwę usługi multimedialnej, z której to polecenie cmdlet pobiera klucze usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="ada9d-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada9d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada9d-113">-ResourceGroupName</span></span>
<span data-ttu-id="ada9d-114">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="ada9d-114">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada9d-115">-DefaultProfile</span></span>
<span data-ttu-id="ada9d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ada9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada9d-117">CommonParameters</span></span>
<span data-ttu-id="ada9d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada9d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada9d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada9d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada9d-120">INPUTS</span></span>

## <span data-ttu-id="ada9d-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ada9d-121">OUTPUTS</span></span>

### <span data-ttu-id="ada9d-122">Microsoft. Azure. Commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="ada9d-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="ada9d-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ada9d-123">NOTES</span></span>

## <span data-ttu-id="ada9d-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada9d-124">RELATED LINKS</span></span>

[<span data-ttu-id="ada9d-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="ada9d-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


