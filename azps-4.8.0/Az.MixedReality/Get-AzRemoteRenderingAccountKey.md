---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064416"
---
# <span data-ttu-id="b1185-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="b1185-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="b1185-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1185-102">SYNOPSIS</span></span>
<span data-ttu-id="b1185-103">Uzyskiwanie kluczy zdalnego konta renderowania</span><span class="sxs-lookup"><span data-stu-id="b1185-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="b1185-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1185-104">SYNTAX</span></span>

### <span data-ttu-id="b1185-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1185-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1185-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1185-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1185-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1185-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1185-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1185-108">DESCRIPTION</span></span>
<span data-ttu-id="b1185-109">Pobierz klawisze deweloperskie konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b1185-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="b1185-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1185-110">EXAMPLES</span></span>

### <span data-ttu-id="b1185-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1185-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="b1185-112">Pobierz klucze dewelopera z konta renderowania zdalnego "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="b1185-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="b1185-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b1185-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="b1185-114">Pobierz klucze dewelopera z konta renderowania zdalnego "przykład" z bieżącego abonamentu i grupy zasobów "RG1" z potokiem.</span><span class="sxs-lookup"><span data-stu-id="b1185-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="b1185-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1185-115">PARAMETERS</span></span>

### <span data-ttu-id="b1185-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1185-116">-DefaultProfile</span></span>
<span data-ttu-id="b1185-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1185-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1185-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1185-118">-InputObject</span></span>
<span data-ttu-id="b1185-119">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="b1185-119">The custom domain object.</span></span>

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

### <span data-ttu-id="b1185-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1185-120">-Name</span></span>
<span data-ttu-id="b1185-121">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b1185-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="b1185-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1185-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1185-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1185-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1185-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1185-124">-ResourceId</span></span>
<span data-ttu-id="b1185-125">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b1185-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="b1185-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1185-126">CommonParameters</span></span>
<span data-ttu-id="b1185-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1185-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1185-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1185-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1185-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1185-129">INPUTS</span></span>

### <span data-ttu-id="b1185-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b1185-130">System.String</span></span>

### <span data-ttu-id="b1185-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b1185-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="b1185-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1185-132">OUTPUTS</span></span>

### <span data-ttu-id="b1185-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b1185-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="b1185-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1185-134">NOTES</span></span>

## <span data-ttu-id="b1185-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1185-135">RELATED LINKS</span></span>
