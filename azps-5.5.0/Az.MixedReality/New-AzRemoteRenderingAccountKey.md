---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180203"
---
# <span data-ttu-id="99f82-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="99f82-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="99f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f82-102">SYNOPSIS</span></span>
<span data-ttu-id="99f82-103">Generuj ponownie klucz konta renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="99f82-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="99f82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99f82-104">SYNTAX</span></span>

### <span data-ttu-id="99f82-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f82-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f82-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f82-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f82-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f82-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f82-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f82-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="99f82-111">DESCRIPTION</span></span>
<span data-ttu-id="99f82-112">Ponownie generuj klucz podstawowy lub klucz pomocniczy konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="99f82-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="99f82-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99f82-113">EXAMPLES</span></span>

### <span data-ttu-id="99f82-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99f82-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="99f82-115">Ponownie wygeneruj klucz pomocniczy konta renderowania zdalnego w "przykładzie" w grupie zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="99f82-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="99f82-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99f82-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="99f82-117">Ponownie wygeneruj klucz pomocniczy "przykład" konta renderowania zdalnego z bieżącej grupy subskrypcji i zasobów "rg1" za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="99f82-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="99f82-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99f82-118">PARAMETERS</span></span>

### <span data-ttu-id="99f82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f82-119">-DefaultProfile</span></span>
<span data-ttu-id="99f82-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99f82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f82-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="99f82-121">-Force</span></span>
<span data-ttu-id="99f82-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="99f82-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99f82-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99f82-123">-InputObject</span></span>
<span data-ttu-id="99f82-124">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="99f82-124">The custom domain object.</span></span>

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

### <span data-ttu-id="99f82-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99f82-125">-Name</span></span>
<span data-ttu-id="99f82-126">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="99f82-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="99f82-127">— Podstawowy</span><span class="sxs-lookup"><span data-stu-id="99f82-127">-Primary</span></span>
<span data-ttu-id="99f82-128">Ponownie generuj klucz podstawowy konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="99f82-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="99f82-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f82-129">-ResourceGroupName</span></span>
<span data-ttu-id="99f82-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99f82-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="99f82-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f82-131">-ResourceId</span></span>
<span data-ttu-id="99f82-132">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="99f82-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="99f82-133">— pomocniczy</span><span class="sxs-lookup"><span data-stu-id="99f82-133">-Secondary</span></span>
<span data-ttu-id="99f82-134">Ponownie generuj klucz podstawowy konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="99f82-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="99f82-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99f82-135">-Confirm</span></span>
<span data-ttu-id="99f82-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99f82-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f82-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f82-137">-WhatIf</span></span>
<span data-ttu-id="99f82-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f82-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99f82-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99f82-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f82-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f82-140">CommonParameters</span></span>
<span data-ttu-id="99f82-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f82-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99f82-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f82-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f82-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99f82-143">INPUTS</span></span>

### <span data-ttu-id="99f82-144">System.String</span><span class="sxs-lookup"><span data-stu-id="99f82-144">System.String</span></span>

### <span data-ttu-id="99f82-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="99f82-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="99f82-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99f82-146">OUTPUTS</span></span>

### <span data-ttu-id="99f82-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99f82-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="99f82-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99f82-148">NOTES</span></span>

## <span data-ttu-id="99f82-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99f82-149">RELATED LINKS</span></span>
