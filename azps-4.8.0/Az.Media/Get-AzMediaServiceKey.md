---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222467"
---
# <span data-ttu-id="7a6ba-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="7a6ba-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="7a6ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6ba-103">Pobiera kluczowe informacje dotyczące uzyskiwania dostępu do punktu końcowego usługi w usłudze multimediów skojarzonego z usługą Media.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="7a6ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a6ba-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a6ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6ba-106">Polecenie cmdlet **Get-AzMediaServiceKey** pobiera informacje kluczowe o uzyskiwaniu dostępu do punktu końcowego przenoszenia stanu (pozostałej) skojarzonego z usługą Azure Media.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="7a6ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6ba-108">Przykład 1: uzyskiwanie najważniejszych informacji dotyczących uzyskiwania dostępu do usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="7a6ba-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="7a6ba-109">To polecenie pobiera kluczowe informacje dotyczące uzyskiwania dostępu do usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="7a6ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a6ba-110">PARAMETERS</span></span>

### <span data-ttu-id="7a6ba-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a6ba-111">-AccountName</span></span>
<span data-ttu-id="7a6ba-112">Określa nazwę usługi multimedialnej, z której to polecenie cmdlet pobiera klucze usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="7a6ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6ba-113">-DefaultProfile</span></span>
<span data-ttu-id="7a6ba-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a6ba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a6ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a6ba-116">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="7a6ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6ba-117">CommonParameters</span></span>
<span data-ttu-id="7a6ba-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6ba-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6ba-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6ba-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a6ba-120">INPUTS</span></span>

### <span data-ttu-id="7a6ba-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7a6ba-121">System.String</span></span>

## <span data-ttu-id="7a6ba-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a6ba-122">OUTPUTS</span></span>

### <span data-ttu-id="7a6ba-123">Microsoft. Azure. Commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="7a6ba-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="7a6ba-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a6ba-124">NOTES</span></span>

## <span data-ttu-id="7a6ba-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a6ba-125">RELATED LINKS</span></span>

[<span data-ttu-id="7a6ba-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="7a6ba-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


