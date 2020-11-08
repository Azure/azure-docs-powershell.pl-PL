---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224134"
---
# <span data-ttu-id="6c1c2-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6c1c2-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="6c1c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1c2-103">Tworzy nowy udział na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="6c1c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c1c2-104">SYNTAX</span></span>

### <span data-ttu-id="6c1c2-105">SmbParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c1c2-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c1c2-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c1c2-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c1c2-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c1c2-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c1c2-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c1c2-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c1c2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6c1c2-109">DESCRIPTION</span></span>
<span data-ttu-id="6c1c2-110">Polecenie cmdlet **New-AzStackEdgeShare** tworzy nowy udział na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="6c1c2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c1c2-111">EXAMPLES</span></span>

### <span data-ttu-id="6c1c2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c1c2-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="6c1c2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c1c2-113">PARAMETERS</span></span>

### <span data-ttu-id="6c1c2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c1c2-114">-AsJob</span></span>
<span data-ttu-id="6c1c2-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6c1c2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c1c2-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="6c1c2-116">-ClientAccessRight</span></span>
<span data-ttu-id="6c1c2-117">Dostęp do odczytu/zapisu dla clientIds, na przykład @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="6c1c2-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="6c1c2-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="6c1c2-118">-CloudShare</span></span>
<span data-ttu-id="6c1c2-119">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6c1c2-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="6c1c2-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6c1c2-120">-ContainerName</span></span>
<span data-ttu-id="6c1c2-121">Nazwa kontenera (na podstawie określonego formatu danych oznacza nazwę pliku systemu Azure/obiektu BLOB Pageblob/Block)</span><span class="sxs-lookup"><span data-stu-id="6c1c2-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="6c1c2-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="6c1c2-122">-DataFormat</span></span>
<span data-ttu-id="6c1c2-123">Ustaw format danych: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="6c1c2-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="6c1c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1c2-124">-DefaultProfile</span></span>
<span data-ttu-id="6c1c2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c1c2-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c1c2-126">-DeviceName</span></span>
<span data-ttu-id="6c1c2-127">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6c1c2-127">Device Name</span></span>

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

### <span data-ttu-id="6c1c2-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c1c2-128">-Name</span></span>
<span data-ttu-id="6c1c2-129">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6c1c2-129">Resource Name</span></span>

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

### <span data-ttu-id="6c1c2-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="6c1c2-130">-NFS</span></span>
<span data-ttu-id="6c1c2-131">AccessProtocol w przypadku tworzenia udziału</span><span class="sxs-lookup"><span data-stu-id="6c1c2-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="6c1c2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1c2-132">-ResourceGroupName</span></span>
<span data-ttu-id="6c1c2-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c1c2-133">Resource Group Name</span></span>

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

### <span data-ttu-id="6c1c2-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="6c1c2-134">-SMB</span></span>
<span data-ttu-id="6c1c2-135">AccessProtocol w przypadku tworzenia udziału</span><span class="sxs-lookup"><span data-stu-id="6c1c2-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="6c1c2-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="6c1c2-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="6c1c2-137">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6c1c2-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="6c1c2-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="6c1c2-138">-UserAccessRight</span></span>
<span data-ttu-id="6c1c2-139">udzielanie praw dostępu wraz z istniejącymi nazwami użytkowników w celu uzyskania dostępu do typów udziałów SMB, na przykład @ (@ {"username" = "User-Name-1"; " AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-2 ";" AccessRight "=" read "}, @ {" NazwaUżytkownika "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="6c1c2-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="6c1c2-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c1c2-140">-Confirm</span></span>
<span data-ttu-id="6c1c2-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1c2-142">-WhatIf</span></span>
<span data-ttu-id="6c1c2-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c1c2-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1c2-145">CommonParameters</span></span>
<span data-ttu-id="6c1c2-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c1c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1c2-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c1c2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1c2-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c1c2-148">INPUTS</span></span>

### <span data-ttu-id="6c1c2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6c1c2-149">System.String</span></span>

## <span data-ttu-id="6c1c2-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c1c2-150">OUTPUTS</span></span>

### <span data-ttu-id="6c1c2-151">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6c1c2-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="6c1c2-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c1c2-152">NOTES</span></span>

## <span data-ttu-id="6c1c2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c1c2-153">RELATED LINKS</span></span>
