---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 0c3494e96290702c424a8e8bac7680daa376c488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994869"
---
# <span data-ttu-id="20901-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="20901-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="20901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20901-102">SYNOPSIS</span></span>
<span data-ttu-id="20901-103">Ustawia nowe hasło dla użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="20901-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="20901-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20901-104">SYNTAX</span></span>

### <span data-ttu-id="20901-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="20901-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20901-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20901-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20901-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20901-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20901-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="20901-108">DESCRIPTION</span></span>
<span data-ttu-id="20901-109">Polecenie **cmdlet Set-AzStackEdgeUser** ustawia nowe hasło dla użytkownika na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="20901-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="20901-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20901-110">EXAMPLES</span></span>

### <span data-ttu-id="20901-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20901-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="20901-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20901-112">PARAMETERS</span></span>

### <span data-ttu-id="20901-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="20901-113">-AsJob</span></span>
<span data-ttu-id="20901-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="20901-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20901-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20901-115">-DefaultProfile</span></span>
<span data-ttu-id="20901-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20901-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20901-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="20901-117">-DeviceName</span></span>
<span data-ttu-id="20901-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="20901-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20901-119">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="20901-119">-EncryptionKey</span></span>
<span data-ttu-id="20901-120">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="20901-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20901-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20901-121">-InputObject</span></span>
<span data-ttu-id="20901-122">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="20901-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20901-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="20901-123">-Name</span></span>
<span data-ttu-id="20901-124">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="20901-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20901-125">— Hasło</span><span class="sxs-lookup"><span data-stu-id="20901-125">-Password</span></span>
<span data-ttu-id="20901-126">Hasło, podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="20901-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20901-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20901-127">-ResourceGroupName</span></span>
<span data-ttu-id="20901-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="20901-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20901-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20901-129">-ResourceId</span></span>
<span data-ttu-id="20901-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="20901-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20901-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20901-131">-Confirm</span></span>
<span data-ttu-id="20901-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20901-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20901-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20901-133">-WhatIf</span></span>
<span data-ttu-id="20901-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20901-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20901-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="20901-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20901-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20901-136">CommonParameters</span></span>
<span data-ttu-id="20901-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20901-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20901-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20901-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20901-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20901-139">INPUTS</span></span>

### <span data-ttu-id="20901-140">Brak</span><span class="sxs-lookup"><span data-stu-id="20901-140">None</span></span>

## <span data-ttu-id="20901-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20901-141">OUTPUTS</span></span>

### <span data-ttu-id="20901-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="20901-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="20901-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20901-143">NOTES</span></span>

## <span data-ttu-id="20901-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20901-144">RELATED LINKS</span></span>
