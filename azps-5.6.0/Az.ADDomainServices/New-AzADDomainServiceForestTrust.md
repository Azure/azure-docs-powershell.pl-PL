---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986315"
---
# <span data-ttu-id="5f8d5-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="5f8d5-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="5f8d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8d5-103">Tworzenie obiektu w pamięci dla aplikacji ForestTrust</span><span class="sxs-lookup"><span data-stu-id="5f8d5-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="5f8d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f8d5-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="5f8d5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8d5-106">Tworzenie obiektu w pamięci dla aplikacji ForestTrust</span><span class="sxs-lookup"><span data-stu-id="5f8d5-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="5f8d5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f8d5-107">EXAMPLES</span></span>

### <span data-ttu-id="5f8d5-108">Przykład 1. Tworzenie oprogramowania ServiceForestTrust dla domeny ADDomain</span><span class="sxs-lookup"><span data-stu-id="5f8d5-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="5f8d5-109">Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="5f8d5-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="5f8d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f8d5-110">PARAMETERS</span></span>

### <span data-ttu-id="5f8d5-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f8d5-111">-FriendlyName</span></span>
<span data-ttu-id="5f8d5-112">Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-112">Friendly Name.</span></span>

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

### <span data-ttu-id="5f8d5-113">- RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="5f8d5-113">-RemoteDnsIP</span></span>
<span data-ttu-id="5f8d5-114">Zdalne adresy IP DNS.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="5f8d5-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="5f8d5-115">-TrustDirection</span></span>
<span data-ttu-id="5f8d5-116">Kierunek zaufania.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-116">Trust Direction.</span></span>

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

### <span data-ttu-id="5f8d5-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="5f8d5-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="5f8d5-118">Nazwa FQDN zaufanej domeny.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="5f8d5-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="5f8d5-119">-TrustPassword</span></span>
<span data-ttu-id="5f8d5-120">Hasło do zaufania.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8d5-121">CommonParameters</span></span>
<span data-ttu-id="5f8d5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8d5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f8d5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8d5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8d5-124">INPUTS</span></span>

## <span data-ttu-id="5f8d5-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8d5-125">OUTPUTS</span></span>

### <span data-ttu-id="5f8d5-126">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="5f8d5-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="5f8d5-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f8d5-127">NOTES</span></span>

<span data-ttu-id="5f8d5-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5f8d5-128">ALIASES</span></span>

## <span data-ttu-id="5f8d5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f8d5-129">RELATED LINKS</span></span>

