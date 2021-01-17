---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339478"
---
# <span data-ttu-id="6e80b-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="6e80b-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="6e80b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e80b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e80b-103">Ponowne generowanie klucza konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="6e80b-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="6e80b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e80b-104">SYNTAX</span></span>

### <span data-ttu-id="6e80b-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e80b-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e80b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e80b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e80b-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e80b-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e80b-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e80b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="6e80b-111">DESCRIPTION</span></span>
<span data-ttu-id="6e80b-112">Ponowne generowanie klucza podstawowego lub klucza pomocniczego konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="6e80b-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="6e80b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e80b-113">EXAMPLES</span></span>

### <span data-ttu-id="6e80b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e80b-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="6e80b-115">Ponownie wygenerować pomocniczy klucz konta renderowania zdalnego "przykład" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="6e80b-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="6e80b-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e80b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6e80b-117">Ponownie wygenerować pomocniczy klucz konta renderowania zdalnego "przykład" z bieżącego abonamentu i grupy zasobów "RG1" z potokiem.</span><span class="sxs-lookup"><span data-stu-id="6e80b-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="6e80b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e80b-118">PARAMETERS</span></span>

### <span data-ttu-id="6e80b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e80b-119">-DefaultProfile</span></span>
<span data-ttu-id="6e80b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e80b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e80b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6e80b-121">-Force</span></span>
<span data-ttu-id="6e80b-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6e80b-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e80b-123">-InputObject</span></span>
<span data-ttu-id="6e80b-124">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="6e80b-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e80b-125">-Name</span></span>
<span data-ttu-id="6e80b-126">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="6e80b-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="6e80b-127">-Primary</span></span>
<span data-ttu-id="6e80b-128">Ponowne generowanie klucza podstawowego konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="6e80b-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e80b-129">-ResourceGroupName</span></span>
<span data-ttu-id="6e80b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e80b-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e80b-131">-ResourceId</span></span>
<span data-ttu-id="6e80b-132">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="6e80b-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-133">-Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="6e80b-133">-Secondary</span></span>
<span data-ttu-id="6e80b-134">Ponowne generowanie klucza podstawowego konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="6e80b-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e80b-135">-Confirm</span></span>
<span data-ttu-id="6e80b-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e80b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e80b-137">-WhatIf</span></span>
<span data-ttu-id="6e80b-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e80b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e80b-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e80b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e80b-140">CommonParameters</span></span>
<span data-ttu-id="6e80b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e80b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6e80b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e80b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e80b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e80b-143">INPUTS</span></span>

### <span data-ttu-id="6e80b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6e80b-144">System.String</span></span>

### <span data-ttu-id="6e80b-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="6e80b-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="6e80b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e80b-146">OUTPUTS</span></span>

### <span data-ttu-id="6e80b-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e80b-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="6e80b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e80b-148">NOTES</span></span>

## <span data-ttu-id="6e80b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e80b-149">RELATED LINKS</span></span>
