---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176595"
---
# <span data-ttu-id="1006e-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="1006e-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="1006e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1006e-102">SYNOPSIS</span></span>
<span data-ttu-id="1006e-103">Tworzenie obiektu w pamięci dla aplikacji ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1006e-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="1006e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1006e-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="1006e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1006e-105">DESCRIPTION</span></span>
<span data-ttu-id="1006e-106">Tworzenie obiektu w pamięci dla aplikacji ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1006e-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="1006e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1006e-107">EXAMPLES</span></span>

### <span data-ttu-id="1006e-108">Przykład 1. Tworzenie oprogramowania ServiceForestTrust dla domeny ADDomain</span><span class="sxs-lookup"><span data-stu-id="1006e-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="1006e-109">Create ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="1006e-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="1006e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1006e-110">PARAMETERS</span></span>

### <span data-ttu-id="1006e-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1006e-111">-FriendlyName</span></span>
<span data-ttu-id="1006e-112">Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="1006e-112">Friendly Name.</span></span>

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

### <span data-ttu-id="1006e-113">- RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="1006e-113">-RemoteDnsIP</span></span>
<span data-ttu-id="1006e-114">Zdalne adresy IP DNS.</span><span class="sxs-lookup"><span data-stu-id="1006e-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="1006e-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="1006e-115">-TrustDirection</span></span>
<span data-ttu-id="1006e-116">Kierunek zaufania.</span><span class="sxs-lookup"><span data-stu-id="1006e-116">Trust Direction.</span></span>

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

### <span data-ttu-id="1006e-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="1006e-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="1006e-118">Nazwa FQDN zaufanej domeny.</span><span class="sxs-lookup"><span data-stu-id="1006e-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="1006e-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="1006e-119">-TrustPassword</span></span>
<span data-ttu-id="1006e-120">Hasło do zaufania.</span><span class="sxs-lookup"><span data-stu-id="1006e-120">Trust Password.</span></span>

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

### <span data-ttu-id="1006e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1006e-121">CommonParameters</span></span>
<span data-ttu-id="1006e-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1006e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1006e-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1006e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1006e-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1006e-124">INPUTS</span></span>

## <span data-ttu-id="1006e-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1006e-125">OUTPUTS</span></span>

### <span data-ttu-id="1006e-126">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1006e-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="1006e-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1006e-127">NOTES</span></span>

<span data-ttu-id="1006e-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1006e-128">ALIASES</span></span>

## <span data-ttu-id="1006e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1006e-129">RELATED LINKS</span></span>

