---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501169"
---
# <span data-ttu-id="41945-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="41945-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="41945-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41945-102">SYNOPSIS</span></span>
<span data-ttu-id="41945-103">Usuwanie konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="41945-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="41945-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41945-104">SYNTAX</span></span>

### <span data-ttu-id="41945-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41945-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41945-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41945-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41945-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="41945-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41945-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41945-108">DESCRIPTION</span></span>
<span data-ttu-id="41945-109">Usuwanie określonego konta renderowania zdalnego z pewnej grupy abonamentów i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="41945-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="41945-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41945-110">EXAMPLES</span></span>

### <span data-ttu-id="41945-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41945-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="41945-112">Usuń konto renderowania zdalnego "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="41945-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="41945-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41945-113">PARAMETERS</span></span>

### <span data-ttu-id="41945-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41945-114">-Confirm</span></span>
<span data-ttu-id="41945-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41945-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41945-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41945-116">-DefaultProfile</span></span>
<span data-ttu-id="41945-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41945-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41945-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41945-118">-InputObject</span></span>
<span data-ttu-id="41945-119">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="41945-119">The custom domain object.</span></span>

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

### <span data-ttu-id="41945-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41945-120">-Name</span></span>
<span data-ttu-id="41945-121">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="41945-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="41945-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41945-122">-PassThru</span></span>
<span data-ttu-id="41945-123">Zwraca obiekt, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="41945-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41945-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41945-124">-ResourceGroupName</span></span>
<span data-ttu-id="41945-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41945-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="41945-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41945-126">-ResourceId</span></span>
<span data-ttu-id="41945-127">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="41945-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="41945-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41945-128">-WhatIf</span></span>
<span data-ttu-id="41945-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41945-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41945-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41945-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41945-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41945-131">CommonParameters</span></span>
<span data-ttu-id="41945-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41945-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="41945-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41945-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41945-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41945-134">INPUTS</span></span>

### <span data-ttu-id="41945-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41945-135">System.String</span></span>

### <span data-ttu-id="41945-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="41945-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="41945-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41945-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41945-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41945-138">OUTPUTS</span></span>

### <span data-ttu-id="41945-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41945-139">System.Boolean</span></span>

## <span data-ttu-id="41945-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41945-140">NOTES</span></span>

## <span data-ttu-id="41945-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41945-141">RELATED LINKS</span></span>
