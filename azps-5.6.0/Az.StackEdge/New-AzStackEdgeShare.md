---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 0046c23c53afa3e5d2b01d506a8d935020f685c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002938"
---
# <span data-ttu-id="a9bc0-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a9bc0-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="a9bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bc0-103">Tworzy nowy udział na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="a9bc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9bc0-104">SYNTAX</span></span>

### <span data-ttu-id="a9bc0-105">SmbParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a9bc0-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9bc0-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bc0-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9bc0-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bc0-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9bc0-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bc0-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9bc0-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9bc0-109">DESCRIPTION</span></span>
<span data-ttu-id="a9bc0-110">Polecenie **cmdlet New-AzStackEdgeShare** tworzy nowy udział na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="a9bc0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9bc0-111">EXAMPLES</span></span>

### <span data-ttu-id="a9bc0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9bc0-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="a9bc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9bc0-113">PARAMETERS</span></span>

### <span data-ttu-id="a9bc0-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a9bc0-114">-AsJob</span></span>
<span data-ttu-id="a9bc0-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a9bc0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9bc0-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="a9bc0-116">-ClientAccessRight</span></span>
<span data-ttu-id="a9bc0-117">Dostęp do odczytu i zapisu dla identyfikatorów klienckich, na przykład:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="a9bc0-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-118">— CloudShare</span><span class="sxs-lookup"><span data-stu-id="a9bc0-118">-CloudShare</span></span>
<span data-ttu-id="a9bc0-119">Podaj nazwę istniejącego zasobu StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a9bc0-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a9bc0-120">-ContainerName</span></span>
<span data-ttu-id="a9bc0-121">Nazwa kontenera (na podstawie określonego formatu danych odzwierciedla ona nazwę obiektu blob platformy Azure Files/Pageblob/Block)</span><span class="sxs-lookup"><span data-stu-id="a9bc0-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-122">- DataFormat</span><span class="sxs-lookup"><span data-stu-id="a9bc0-122">-DataFormat</span></span>
<span data-ttu-id="a9bc0-123">Ustawianie formatu danych, np.: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="a9bc0-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bc0-124">-DefaultProfile</span></span>
<span data-ttu-id="a9bc0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9bc0-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a9bc0-126">-DeviceName</span></span>
<span data-ttu-id="a9bc0-127">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a9bc0-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9bc0-128">-Name</span></span>
<span data-ttu-id="a9bc0-129">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="a9bc0-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="a9bc0-130">-NFS</span></span>
<span data-ttu-id="a9bc0-131">AccessProtocol w przypadku tworzenia udostępniania</span><span class="sxs-lookup"><span data-stu-id="a9bc0-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bc0-132">-ResourceGroupName</span></span>
<span data-ttu-id="a9bc0-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9bc0-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-134">— SMB</span><span class="sxs-lookup"><span data-stu-id="a9bc0-134">-SMB</span></span>
<span data-ttu-id="a9bc0-135">AccessProtocol w przypadku tworzenia udostępniania</span><span class="sxs-lookup"><span data-stu-id="a9bc0-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="a9bc0-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="a9bc0-137">Podaj nazwę istniejącego zasobu StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a9bc0-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="a9bc0-138">-UserAccessRight</span></span>
<span data-ttu-id="a9bc0-139">zapewnij dostęp bezpośrednio do istniejących nazw użytkowników, aby uzyskać dostęp do typów udostępniania SMB, na przykład: @(@{"Username"="nazwa_użytkownika-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="a9bc0-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc0-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9bc0-140">-Confirm</span></span>
<span data-ttu-id="a9bc0-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9bc0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9bc0-142">-WhatIf</span></span>
<span data-ttu-id="a9bc0-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9bc0-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9bc0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bc0-145">CommonParameters</span></span>
<span data-ttu-id="a9bc0-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bc0-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9bc0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bc0-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9bc0-148">INPUTS</span></span>

### <span data-ttu-id="a9bc0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a9bc0-149">System.String</span></span>

## <span data-ttu-id="a9bc0-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9bc0-150">OUTPUTS</span></span>

### <span data-ttu-id="a9bc0-151">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a9bc0-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="a9bc0-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9bc0-152">NOTES</span></span>

## <span data-ttu-id="a9bc0-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9bc0-153">RELATED LINKS</span></span>
