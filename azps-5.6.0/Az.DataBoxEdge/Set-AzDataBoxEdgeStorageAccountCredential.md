---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 214b43148020b2884013a45f26b4a03cd4ea3736
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971281"
---
# <span data-ttu-id="98fd0-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="98fd0-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="98fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="98fd0-103">Ustawia poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="98fd0-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="98fd0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98fd0-104">SYNTAX</span></span>

### <span data-ttu-id="98fd0-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="98fd0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98fd0-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98fd0-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98fd0-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98fd0-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98fd0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="98fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="98fd0-109">Polecenie **cmdlet Set-AzDataBoxEdgeStorageAccountCredential** aktualizuje poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="98fd0-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="98fd0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98fd0-110">EXAMPLES</span></span>

### <span data-ttu-id="98fd0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98fd0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="98fd0-112">Pomaga w obracaniu klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="98fd0-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="98fd0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98fd0-113">PARAMETERS</span></span>

### <span data-ttu-id="98fd0-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="98fd0-114">-AsJob</span></span>
<span data-ttu-id="98fd0-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="98fd0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98fd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fd0-116">-DefaultProfile</span></span>
<span data-ttu-id="98fd0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="98fd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fd0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="98fd0-118">-DeviceName</span></span>
<span data-ttu-id="98fd0-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="98fd0-119">Device Name</span></span>

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

### <span data-ttu-id="98fd0-120">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="98fd0-120">-EncryptionKey</span></span>
<span data-ttu-id="98fd0-121">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="98fd0-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="98fd0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98fd0-122">-InputObject</span></span>
<span data-ttu-id="98fd0-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="98fd0-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98fd0-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="98fd0-124">-Name</span></span>
<span data-ttu-id="98fd0-125">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="98fd0-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fd0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fd0-126">-ResourceGroupName</span></span>
<span data-ttu-id="98fd0-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="98fd0-127">Resource Group Name</span></span>

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

### <span data-ttu-id="98fd0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98fd0-128">-ResourceId</span></span>
<span data-ttu-id="98fd0-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="98fd0-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="98fd0-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="98fd0-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="98fd0-131">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="98fd0-131">provide storage account access key</span></span>

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

### <span data-ttu-id="98fd0-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98fd0-132">-Confirm</span></span>
<span data-ttu-id="98fd0-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98fd0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fd0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fd0-134">-WhatIf</span></span>
<span data-ttu-id="98fd0-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98fd0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98fd0-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="98fd0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fd0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fd0-137">CommonParameters</span></span>
<span data-ttu-id="98fd0-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fd0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fd0-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98fd0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fd0-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98fd0-140">INPUTS</span></span>

### <span data-ttu-id="98fd0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="98fd0-141">System.String</span></span>

### <span data-ttu-id="98fd0-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="98fd0-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="98fd0-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98fd0-143">OUTPUTS</span></span>

### <span data-ttu-id="98fd0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="98fd0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="98fd0-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98fd0-145">NOTES</span></span>

## <span data-ttu-id="98fd0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98fd0-146">RELATED LINKS</span></span>
