---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194858"
---
# <span data-ttu-id="1cbe0-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1cbe0-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="1cbe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbe0-103">Aktualizuje udostępnianie na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-103">Updates the share for a device.</span></span>

## <span data-ttu-id="1cbe0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1cbe0-104">SYNTAX</span></span>

### <span data-ttu-id="1cbe0-105">SmbParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1cbe0-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cbe0-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cbe0-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbe0-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cbe0-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbe0-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cbe0-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbe0-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cbe0-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbe0-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cbe0-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cbe0-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="1cbe0-111">DESCRIPTION</span></span>
<span data-ttu-id="1cbe0-112">To **ustawienie Set-AzDataBoxEdgeShare** zastąpi prawa dostępu</span><span class="sxs-lookup"><span data-stu-id="1cbe0-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="1cbe0-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1cbe0-113">EXAMPLES</span></span>

### <span data-ttu-id="1cbe0-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1cbe0-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="1cbe0-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1cbe0-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="1cbe0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cbe0-116">PARAMETERS</span></span>

### <span data-ttu-id="1cbe0-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1cbe0-117">-AsJob</span></span>
<span data-ttu-id="1cbe0-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1cbe0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cbe0-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="1cbe0-119">-ClientAccessRight</span></span>
<span data-ttu-id="1cbe0-120">Dostęp do odczytu i zapisu dla identyfikatorów klienta, np.: @(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="1cbe0-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="1cbe0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbe0-121">-DefaultProfile</span></span>
<span data-ttu-id="1cbe0-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cbe0-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1cbe0-123">-DeviceName</span></span>
<span data-ttu-id="1cbe0-124">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="1cbe0-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbe0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cbe0-125">-InputObject</span></span>
<span data-ttu-id="1cbe0-126">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="1cbe0-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbe0-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1cbe0-127">-Name</span></span>
<span data-ttu-id="1cbe0-128">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="1cbe0-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbe0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbe0-129">-ResourceGroupName</span></span>
<span data-ttu-id="1cbe0-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1cbe0-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbe0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cbe0-131">-ResourceId</span></span>
<span data-ttu-id="1cbe0-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cbe0-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="1cbe0-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="1cbe0-133">-UserAccessRight</span></span>
<span data-ttu-id="1cbe0-134">zapewnij dostęp bezpośrednio do istniejących nazw użytkowników, aby uzyskać dostęp do typów udostępniania SMB, na przykład: @(@{"Username"="nazwa_użytkownika-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="1cbe0-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="1cbe0-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cbe0-135">-Confirm</span></span>
<span data-ttu-id="1cbe0-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cbe0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbe0-137">-WhatIf</span></span>
<span data-ttu-id="1cbe0-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cbe0-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cbe0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbe0-140">CommonParameters</span></span>
<span data-ttu-id="1cbe0-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbe0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbe0-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cbe0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbe0-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cbe0-143">INPUTS</span></span>

### <span data-ttu-id="1cbe0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1cbe0-144">System.String</span></span>

### <span data-ttu-id="1cbe0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1cbe0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="1cbe0-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cbe0-146">OUTPUTS</span></span>

### <span data-ttu-id="1cbe0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1cbe0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="1cbe0-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1cbe0-148">NOTES</span></span>

## <span data-ttu-id="1cbe0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cbe0-149">RELATED LINKS</span></span>
