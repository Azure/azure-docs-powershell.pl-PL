---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222162"
---
# <span data-ttu-id="bbe5e-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bbe5e-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="bbe5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbe5e-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe5e-103">Ustawia nowe hasło dla użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="bbe5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbe5e-104">SYNTAX</span></span>

### <span data-ttu-id="bbe5e-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bbe5e-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe5e-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbe5e-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe5e-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbe5e-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe5e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bbe5e-108">DESCRIPTION</span></span>
<span data-ttu-id="bbe5e-109">Polecenie cmdlet **Set-AzStackEdgeUser** ustawia nowe hasło dla użytkownika na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="bbe5e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbe5e-110">EXAMPLES</span></span>

### <span data-ttu-id="bbe5e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbe5e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="bbe5e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbe5e-112">PARAMETERS</span></span>

### <span data-ttu-id="bbe5e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbe5e-113">-AsJob</span></span>
<span data-ttu-id="bbe5e-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bbe5e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbe5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe5e-115">-DefaultProfile</span></span>
<span data-ttu-id="bbe5e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe5e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bbe5e-117">-DeviceName</span></span>
<span data-ttu-id="bbe5e-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="bbe5e-118">Device Name</span></span>

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

### <span data-ttu-id="bbe5e-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bbe5e-119">-EncryptionKey</span></span>
<span data-ttu-id="bbe5e-120">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="bbe5e-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bbe5e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bbe5e-121">-InputObject</span></span>
<span data-ttu-id="bbe5e-122">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="bbe5e-122">Input Object</span></span>

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

### <span data-ttu-id="bbe5e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbe5e-123">-Name</span></span>
<span data-ttu-id="bbe5e-124">Nazwie</span><span class="sxs-lookup"><span data-stu-id="bbe5e-124">Username</span></span>

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

### <span data-ttu-id="bbe5e-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="bbe5e-125">-Password</span></span>
<span data-ttu-id="bbe5e-126">Hasło podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="bbe5e-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="bbe5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="bbe5e-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bbe5e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bbe5e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe5e-129">-ResourceId</span></span>
<span data-ttu-id="bbe5e-130">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bbe5e-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="bbe5e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbe5e-131">-Confirm</span></span>
<span data-ttu-id="bbe5e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe5e-133">-WhatIf</span></span>
<span data-ttu-id="bbe5e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbe5e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe5e-136">CommonParameters</span></span>
<span data-ttu-id="bbe5e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe5e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbe5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe5e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbe5e-139">INPUTS</span></span>

### <span data-ttu-id="bbe5e-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bbe5e-140">None</span></span>

## <span data-ttu-id="bbe5e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbe5e-141">OUTPUTS</span></span>

### <span data-ttu-id="bbe5e-142">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bbe5e-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="bbe5e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbe5e-143">NOTES</span></span>

## <span data-ttu-id="bbe5e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbe5e-144">RELATED LINKS</span></span>
