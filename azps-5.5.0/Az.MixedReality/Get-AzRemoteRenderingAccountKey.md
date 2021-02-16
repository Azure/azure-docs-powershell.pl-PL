---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194091"
---
# <span data-ttu-id="e35a8-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="e35a8-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="e35a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e35a8-103">Uzyskiwanie kluczy konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="e35a8-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="e35a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e35a8-104">SYNTAX</span></span>

### <span data-ttu-id="e35a8-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e35a8-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35a8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35a8-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35a8-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35a8-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35a8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e35a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e35a8-109">Uzyskaj klucze dewelopera konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e35a8-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="e35a8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e35a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e35a8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e35a8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e35a8-112">Uzyskaj klucze dewelopera "przykład" konta renderowania zdalnego z bieżącej subskrypcji i grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="e35a8-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="e35a8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e35a8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e35a8-114">Uzyskaj klucze dewelopera "przykład" konta renderowania zdalnego z bieżącej subskrypcji i grupy zasobów "rg1" za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="e35a8-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="e35a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e35a8-115">PARAMETERS</span></span>

### <span data-ttu-id="e35a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35a8-116">-DefaultProfile</span></span>
<span data-ttu-id="e35a8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e35a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e35a8-118">-InputObject</span></span>
<span data-ttu-id="e35a8-119">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="e35a8-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e35a8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e35a8-120">-Name</span></span>
<span data-ttu-id="e35a8-121">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e35a8-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="e35a8-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e35a8-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35a8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e35a8-124">-ResourceId</span></span>
<span data-ttu-id="e35a8-125">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="e35a8-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35a8-126">CommonParameters</span></span>
<span data-ttu-id="e35a8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e35a8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35a8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35a8-129">INPUTS</span></span>

### <span data-ttu-id="e35a8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e35a8-130">System.String</span></span>

### <span data-ttu-id="e35a8-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e35a8-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="e35a8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35a8-132">OUTPUTS</span></span>

### <span data-ttu-id="e35a8-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e35a8-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="e35a8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e35a8-134">NOTES</span></span>

## <span data-ttu-id="e35a8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e35a8-135">RELATED LINKS</span></span>
