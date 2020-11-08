---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221304"
---
# <span data-ttu-id="897d7-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="897d7-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="897d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="897d7-102">SYNOPSIS</span></span>
<span data-ttu-id="897d7-103">Ustawia poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="897d7-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="897d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="897d7-104">SYNTAX</span></span>

### <span data-ttu-id="897d7-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="897d7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897d7-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="897d7-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="897d7-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="897d7-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897d7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="897d7-108">DESCRIPTION</span></span>
<span data-ttu-id="897d7-109">Polecenie cmdlet **Set-AzDataBoxEdgeStorageAccountCredential** aktualizuje poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="897d7-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="897d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="897d7-110">EXAMPLES</span></span>

### <span data-ttu-id="897d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="897d7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="897d7-112">Pomaga w obracaniu klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="897d7-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="897d7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="897d7-113">PARAMETERS</span></span>

### <span data-ttu-id="897d7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="897d7-114">-AsJob</span></span>
<span data-ttu-id="897d7-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="897d7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="897d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897d7-116">-DefaultProfile</span></span>
<span data-ttu-id="897d7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="897d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897d7-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="897d7-118">-DeviceName</span></span>
<span data-ttu-id="897d7-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="897d7-119">Device Name</span></span>

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

### <span data-ttu-id="897d7-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="897d7-120">-EncryptionKey</span></span>
<span data-ttu-id="897d7-121">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="897d7-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="897d7-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="897d7-122">-InputObject</span></span>
<span data-ttu-id="897d7-123">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="897d7-123">Input Object</span></span>

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

### <span data-ttu-id="897d7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="897d7-124">-Name</span></span>
<span data-ttu-id="897d7-125">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="897d7-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="897d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="897d7-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="897d7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="897d7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="897d7-128">-ResourceId</span></span>
<span data-ttu-id="897d7-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="897d7-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="897d7-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="897d7-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="897d7-131">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="897d7-131">provide storage account access key</span></span>

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

### <span data-ttu-id="897d7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="897d7-132">-Confirm</span></span>
<span data-ttu-id="897d7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897d7-134">-WhatIf</span></span>
<span data-ttu-id="897d7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897d7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="897d7-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="897d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897d7-137">CommonParameters</span></span>
<span data-ttu-id="897d7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897d7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="897d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897d7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="897d7-140">INPUTS</span></span>

### <span data-ttu-id="897d7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="897d7-141">System.String</span></span>

### <span data-ttu-id="897d7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="897d7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="897d7-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="897d7-143">OUTPUTS</span></span>

### <span data-ttu-id="897d7-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="897d7-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="897d7-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="897d7-145">NOTES</span></span>

## <span data-ttu-id="897d7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="897d7-146">RELATED LINKS</span></span>
