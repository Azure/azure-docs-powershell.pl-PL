---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: a2de03f28935fb8002966e0e9251218809ddec5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971274"
---
# <span data-ttu-id="6641b-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6641b-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="6641b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6641b-102">SYNOPSIS</span></span>
<span data-ttu-id="6641b-103">Ustawia nowe hasło dla użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6641b-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="6641b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6641b-104">SYNTAX</span></span>

### <span data-ttu-id="6641b-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6641b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6641b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6641b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6641b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6641b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6641b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6641b-108">DESCRIPTION</span></span>
<span data-ttu-id="6641b-109">Polecenie **cmdlet Set-AzDataBoxEdgeUser** ustawia nowe hasło dla użytkownika na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="6641b-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="6641b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6641b-110">EXAMPLES</span></span>

### <span data-ttu-id="6641b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6641b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="6641b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6641b-112">PARAMETERS</span></span>

### <span data-ttu-id="6641b-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6641b-113">-AsJob</span></span>
<span data-ttu-id="6641b-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6641b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6641b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6641b-115">-DefaultProfile</span></span>
<span data-ttu-id="6641b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6641b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6641b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6641b-117">-DeviceName</span></span>
<span data-ttu-id="6641b-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6641b-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6641b-119">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="6641b-119">-EncryptionKey</span></span>
<span data-ttu-id="6641b-120">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="6641b-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="6641b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6641b-121">-InputObject</span></span>
<span data-ttu-id="6641b-122">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="6641b-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6641b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6641b-123">-Name</span></span>
<span data-ttu-id="6641b-124">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="6641b-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6641b-125">— Hasło</span><span class="sxs-lookup"><span data-stu-id="6641b-125">-Password</span></span>
<span data-ttu-id="6641b-126">Hasło, podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="6641b-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="6641b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6641b-127">-ResourceGroupName</span></span>
<span data-ttu-id="6641b-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6641b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6641b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6641b-129">-ResourceId</span></span>
<span data-ttu-id="6641b-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6641b-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6641b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6641b-131">-Confirm</span></span>
<span data-ttu-id="6641b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6641b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6641b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6641b-133">-WhatIf</span></span>
<span data-ttu-id="6641b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6641b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6641b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6641b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6641b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6641b-136">CommonParameters</span></span>
<span data-ttu-id="6641b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6641b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6641b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6641b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6641b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6641b-139">INPUTS</span></span>

### <span data-ttu-id="6641b-140">Brak</span><span class="sxs-lookup"><span data-stu-id="6641b-140">None</span></span>

## <span data-ttu-id="6641b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6641b-141">OUTPUTS</span></span>

### <span data-ttu-id="6641b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6641b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="6641b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6641b-143">NOTES</span></span>

## <span data-ttu-id="6641b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6641b-144">RELATED LINKS</span></span>
