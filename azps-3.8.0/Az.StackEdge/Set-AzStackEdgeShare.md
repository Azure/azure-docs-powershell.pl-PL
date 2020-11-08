---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052861"
---
# <span data-ttu-id="c3cdc-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3cdc-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="c3cdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cdc-103">Umożliwia zaktualizowanie udziału urządzenia.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-103">Updates the share for a device.</span></span>

## <span data-ttu-id="c3cdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3cdc-104">SYNTAX</span></span>

### <span data-ttu-id="c3cdc-105">SmbParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3cdc-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3cdc-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cdc-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cdc-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cdc-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cdc-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cdc-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cdc-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cdc-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cdc-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cdc-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3cdc-111">Opis</span><span class="sxs-lookup"><span data-stu-id="c3cdc-111">DESCRIPTION</span></span>
<span data-ttu-id="c3cdc-112">Ten **zestaw-AzStackEdgeShare** zamieni prawa dostępu</span><span class="sxs-lookup"><span data-stu-id="c3cdc-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="c3cdc-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3cdc-113">EXAMPLES</span></span>

### <span data-ttu-id="c3cdc-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3cdc-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="c3cdc-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c3cdc-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="c3cdc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3cdc-116">PARAMETERS</span></span>

### <span data-ttu-id="c3cdc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3cdc-117">-AsJob</span></span>
<span data-ttu-id="c3cdc-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c3cdc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3cdc-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="c3cdc-119">-ClientAccessRight</span></span>
<span data-ttu-id="c3cdc-120">Dostęp do odczytu/zapisu dla clientIds, na przykład @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="c3cdc-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cdc-121">-DefaultProfile</span></span>
<span data-ttu-id="c3cdc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cdc-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c3cdc-123">-DeviceName</span></span>
<span data-ttu-id="c3cdc-124">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="c3cdc-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3cdc-125">-InputObject</span></span>
<span data-ttu-id="c3cdc-126">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="c3cdc-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3cdc-127">-Name</span></span>
<span data-ttu-id="c3cdc-128">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="c3cdc-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cdc-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3cdc-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c3cdc-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3cdc-131">-ResourceId</span></span>
<span data-ttu-id="c3cdc-132">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c3cdc-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="c3cdc-133">-UserAccessRight</span></span>
<span data-ttu-id="c3cdc-134">udzielanie praw dostępu wraz z istniejącymi nazwami użytkowników w celu uzyskania dostępu do typów udziałów SMB, na przykład @ (@ {"username" = "User-Name-1"; " AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-2 ";" AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="c3cdc-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3cdc-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3cdc-135">-Confirm</span></span>
<span data-ttu-id="c3cdc-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cdc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cdc-137">-WhatIf</span></span>
<span data-ttu-id="c3cdc-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3cdc-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cdc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cdc-140">CommonParameters</span></span>
<span data-ttu-id="c3cdc-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cdc-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3cdc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cdc-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3cdc-143">INPUTS</span></span>

### <span data-ttu-id="c3cdc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c3cdc-144">System.String</span></span>

### <span data-ttu-id="c3cdc-145">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3cdc-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="c3cdc-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3cdc-146">OUTPUTS</span></span>

### <span data-ttu-id="c3cdc-147">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3cdc-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="c3cdc-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3cdc-148">NOTES</span></span>

## <span data-ttu-id="c3cdc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3cdc-149">RELATED LINKS</span></span>
