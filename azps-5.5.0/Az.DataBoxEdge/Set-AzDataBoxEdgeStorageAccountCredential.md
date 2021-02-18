---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181059"
---
# <span data-ttu-id="463e1-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="463e1-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="463e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463e1-102">SYNOPSIS</span></span>
<span data-ttu-id="463e1-103">Ustawia poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="463e1-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="463e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="463e1-104">SYNTAX</span></span>

### <span data-ttu-id="463e1-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="463e1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="463e1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="463e1-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="463e1-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="463e1-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463e1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="463e1-108">DESCRIPTION</span></span>
<span data-ttu-id="463e1-109">Polecenie **cmdlet Set-AzDataBoxEdgeStorageAccountCredential** aktualizuje poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="463e1-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="463e1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="463e1-110">EXAMPLES</span></span>

### <span data-ttu-id="463e1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="463e1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="463e1-112">Pomaga w obracaniu klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="463e1-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="463e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463e1-113">PARAMETERS</span></span>

### <span data-ttu-id="463e1-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="463e1-114">-AsJob</span></span>
<span data-ttu-id="463e1-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="463e1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="463e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463e1-116">-DefaultProfile</span></span>
<span data-ttu-id="463e1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="463e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463e1-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="463e1-118">-DeviceName</span></span>
<span data-ttu-id="463e1-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="463e1-119">Device Name</span></span>

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

### <span data-ttu-id="463e1-120">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="463e1-120">-EncryptionKey</span></span>
<span data-ttu-id="463e1-121">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="463e1-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="463e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="463e1-122">-InputObject</span></span>
<span data-ttu-id="463e1-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="463e1-123">Input Object</span></span>

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

### <span data-ttu-id="463e1-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="463e1-124">-Name</span></span>
<span data-ttu-id="463e1-125">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="463e1-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="463e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="463e1-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="463e1-127">Resource Group Name</span></span>

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

### <span data-ttu-id="463e1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="463e1-128">-ResourceId</span></span>
<span data-ttu-id="463e1-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="463e1-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="463e1-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="463e1-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="463e1-131">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="463e1-131">provide storage account access key</span></span>

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

### <span data-ttu-id="463e1-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="463e1-132">-Confirm</span></span>
<span data-ttu-id="463e1-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="463e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463e1-134">-WhatIf</span></span>
<span data-ttu-id="463e1-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463e1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="463e1-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="463e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463e1-137">CommonParameters</span></span>
<span data-ttu-id="463e1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463e1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="463e1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463e1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463e1-140">INPUTS</span></span>

### <span data-ttu-id="463e1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="463e1-141">System.String</span></span>

### <span data-ttu-id="463e1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="463e1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="463e1-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463e1-143">OUTPUTS</span></span>

### <span data-ttu-id="463e1-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="463e1-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="463e1-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="463e1-145">NOTES</span></span>

## <span data-ttu-id="463e1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="463e1-146">RELATED LINKS</span></span>
