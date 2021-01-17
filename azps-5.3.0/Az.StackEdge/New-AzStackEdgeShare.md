---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489329"
---
# <span data-ttu-id="0c59a-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0c59a-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="0c59a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c59a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c59a-103">Tworzy nowy udział na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="0c59a-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="0c59a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c59a-104">SYNTAX</span></span>

### <span data-ttu-id="0c59a-105">SmbParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c59a-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c59a-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c59a-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c59a-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c59a-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c59a-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c59a-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c59a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0c59a-109">DESCRIPTION</span></span>
<span data-ttu-id="0c59a-110">Polecenie cmdlet **New-AzStackEdgeShare** tworzy nowy udział na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="0c59a-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="0c59a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c59a-111">EXAMPLES</span></span>

### <span data-ttu-id="0c59a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c59a-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="0c59a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c59a-113">PARAMETERS</span></span>

### <span data-ttu-id="0c59a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c59a-114">-AsJob</span></span>
<span data-ttu-id="0c59a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c59a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c59a-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="0c59a-116">-ClientAccessRight</span></span>
<span data-ttu-id="0c59a-117">Dostęp do odczytu/zapisu dla clientIds, na przykład @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="0c59a-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="0c59a-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="0c59a-118">-CloudShare</span></span>
<span data-ttu-id="0c59a-119">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0c59a-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="0c59a-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0c59a-120">-ContainerName</span></span>
<span data-ttu-id="0c59a-121">Nazwa kontenera (na podstawie określonego formatu danych oznacza nazwę pliku systemu Azure/obiektu BLOB Pageblob/Block)</span><span class="sxs-lookup"><span data-stu-id="0c59a-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="0c59a-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="0c59a-122">-DataFormat</span></span>
<span data-ttu-id="0c59a-123">Ustaw format danych: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="0c59a-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="0c59a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c59a-124">-DefaultProfile</span></span>
<span data-ttu-id="0c59a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c59a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c59a-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0c59a-126">-DeviceName</span></span>
<span data-ttu-id="0c59a-127">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0c59a-127">Device Name</span></span>

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

### <span data-ttu-id="0c59a-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c59a-128">-Name</span></span>
<span data-ttu-id="0c59a-129">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0c59a-129">Resource Name</span></span>

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

### <span data-ttu-id="0c59a-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="0c59a-130">-NFS</span></span>
<span data-ttu-id="0c59a-131">AccessProtocol w przypadku tworzenia udziału</span><span class="sxs-lookup"><span data-stu-id="0c59a-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="0c59a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c59a-132">-ResourceGroupName</span></span>
<span data-ttu-id="0c59a-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c59a-133">Resource Group Name</span></span>

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

### <span data-ttu-id="0c59a-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="0c59a-134">-SMB</span></span>
<span data-ttu-id="0c59a-135">AccessProtocol w przypadku tworzenia udziału</span><span class="sxs-lookup"><span data-stu-id="0c59a-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="0c59a-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="0c59a-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="0c59a-137">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0c59a-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="0c59a-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="0c59a-138">-UserAccessRight</span></span>
<span data-ttu-id="0c59a-139">udzielanie praw dostępu wraz z istniejącymi nazwami użytkowników w celu uzyskania dostępu do typów udziałów SMB, na przykład @ (@ {"username" = "User-Name-1"; " AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-2 ";" AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="0c59a-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="0c59a-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c59a-140">-Confirm</span></span>
<span data-ttu-id="0c59a-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c59a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c59a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c59a-142">-WhatIf</span></span>
<span data-ttu-id="0c59a-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c59a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c59a-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c59a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c59a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c59a-145">CommonParameters</span></span>
<span data-ttu-id="0c59a-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c59a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c59a-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c59a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c59a-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c59a-148">INPUTS</span></span>

### <span data-ttu-id="0c59a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0c59a-149">System.String</span></span>

## <span data-ttu-id="0c59a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c59a-150">OUTPUTS</span></span>

### <span data-ttu-id="0c59a-151">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0c59a-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="0c59a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c59a-152">NOTES</span></span>

## <span data-ttu-id="0c59a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c59a-153">RELATED LINKS</span></span>
