---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180251"
---
# <span data-ttu-id="8950c-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8950c-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="8950c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8950c-102">SYNOPSIS</span></span>
<span data-ttu-id="8950c-103">Pobiera kluczowe informacje dotyczące uzyskiwania dostępu do punktu końcowego REST skojarzonego z usługą multimediów.</span><span class="sxs-lookup"><span data-stu-id="8950c-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="8950c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8950c-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8950c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8950c-105">DESCRIPTION</span></span>
<span data-ttu-id="8950c-106">Polecenie **cmdlet Get-AzMediaServiceKey** pobiera najważniejsze informacje dotyczące uzyskiwania dostępu do punktu końcowego REST (Representational State Transfer) skojarzonego z usługą multimediów Azure.</span><span class="sxs-lookup"><span data-stu-id="8950c-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="8950c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8950c-107">EXAMPLES</span></span>

### <span data-ttu-id="8950c-108">Przykład 1. Uzyskiwanie kluczowych informacji dotyczących uzyskiwania dostępu do usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="8950c-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="8950c-109">To polecenie pobiera najważniejsze informacje dotyczące uzyskiwania dostępu do usługi multimediów o nazwie MediaService001, która należy do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="8950c-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="8950c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8950c-110">PARAMETERS</span></span>

### <span data-ttu-id="8950c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8950c-111">-AccountName</span></span>
<span data-ttu-id="8950c-112">Określa nazwę usługi multimediów, z których to polecenie cmdlet pobiera klucze usługi multimediów.</span><span class="sxs-lookup"><span data-stu-id="8950c-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="8950c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8950c-113">-DefaultProfile</span></span>
<span data-ttu-id="8950c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8950c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8950c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8950c-115">-ResourceGroupName</span></span>
<span data-ttu-id="8950c-116">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="8950c-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="8950c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8950c-117">CommonParameters</span></span>
<span data-ttu-id="8950c-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8950c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8950c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8950c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8950c-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8950c-120">INPUTS</span></span>

### <span data-ttu-id="8950c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8950c-121">System.String</span></span>

## <span data-ttu-id="8950c-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8950c-122">OUTPUTS</span></span>

### <span data-ttu-id="8950c-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="8950c-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="8950c-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8950c-124">NOTES</span></span>

## <span data-ttu-id="8950c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8950c-125">RELATED LINKS</span></span>

[<span data-ttu-id="8950c-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8950c-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


