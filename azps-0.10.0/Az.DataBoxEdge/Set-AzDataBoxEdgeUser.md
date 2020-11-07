---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: c344d5ac901e45c92c04a23cee252b1f747d4a83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891553"
---
# <span data-ttu-id="b2342-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b2342-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b2342-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2342-102">SYNOPSIS</span></span>
<span data-ttu-id="b2342-103">Ustawia nowe hasło dla użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="b2342-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="b2342-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2342-104">SYNTAX</span></span>

### <span data-ttu-id="b2342-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2342-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2342-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2342-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2342-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2342-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2342-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2342-108">DESCRIPTION</span></span>
<span data-ttu-id="b2342-109">Polecenie cmdlet **Set-AzDataBoxEdgeUser** ustawia nowe hasło dla użytkownika na urządzeniu z krawędziami pola danych.</span><span class="sxs-lookup"><span data-stu-id="b2342-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="b2342-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2342-110">EXAMPLES</span></span>

### <span data-ttu-id="b2342-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2342-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="b2342-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2342-112">PARAMETERS</span></span>

### <span data-ttu-id="b2342-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2342-113">-AsJob</span></span>
<span data-ttu-id="b2342-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2342-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2342-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2342-115">-DefaultProfile</span></span>
<span data-ttu-id="b2342-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2342-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2342-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b2342-117">-DeviceName</span></span>
<span data-ttu-id="b2342-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b2342-118">Device Name</span></span>

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

### <span data-ttu-id="b2342-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2342-119">-EncryptionKey</span></span>
<span data-ttu-id="b2342-120">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="b2342-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b2342-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2342-121">-InputObject</span></span>
<span data-ttu-id="b2342-122">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="b2342-122">Input Object</span></span>

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

### <span data-ttu-id="b2342-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2342-123">-Name</span></span>
<span data-ttu-id="b2342-124">Nazwie</span><span class="sxs-lookup"><span data-stu-id="b2342-124">Username</span></span>

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

### <span data-ttu-id="b2342-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="b2342-125">-Password</span></span>
<span data-ttu-id="b2342-126">Hasło podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="b2342-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="b2342-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2342-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2342-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b2342-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b2342-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2342-129">-ResourceId</span></span>
<span data-ttu-id="b2342-130">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b2342-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="b2342-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2342-131">-Confirm</span></span>
<span data-ttu-id="b2342-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2342-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2342-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2342-133">-WhatIf</span></span>
<span data-ttu-id="b2342-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2342-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2342-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2342-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2342-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2342-136">CommonParameters</span></span>
<span data-ttu-id="b2342-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2342-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2342-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2342-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2342-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2342-139">INPUTS</span></span>

### <span data-ttu-id="b2342-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b2342-140">None</span></span>

## <span data-ttu-id="b2342-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2342-141">OUTPUTS</span></span>

### <span data-ttu-id="b2342-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b2342-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="b2342-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2342-143">NOTES</span></span>

## <span data-ttu-id="b2342-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2342-144">RELATED LINKS</span></span>
