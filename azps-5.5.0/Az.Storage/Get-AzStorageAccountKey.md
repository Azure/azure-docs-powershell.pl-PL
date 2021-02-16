---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197579"
---
# <span data-ttu-id="d0fd6-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0fd6-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="d0fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fd6-103">Pobiera klucze dostępu dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d0fd6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0fd6-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0fd6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0fd6-105">DESCRIPTION</span></span>
<span data-ttu-id="d0fd6-106">Polecenie **cmdlet Get-AzStorageAccountKey** pobiera klucze dostępu dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d0fd6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0fd6-107">EXAMPLES</span></span>

### <span data-ttu-id="d0fd6-108">Przykład 1. Uzyskiwanie kluczy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d0fd6-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d0fd6-109">To polecenie pobiera klucze dla określonego konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="d0fd6-110">Przykład 2. Uzyskiwanie określonego klucza dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d0fd6-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="d0fd6-111">Przykład 3. Zawiera listę kluczy dostępu dla konta magazynu, w tym klucze Kerberos (jeśli włączono usługę Active Directory)</span><span class="sxs-lookup"><span data-stu-id="d0fd6-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="d0fd6-112">To polecenie pobiera klucze dla określonego konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="d0fd6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0fd6-113">PARAMETERS</span></span>

### <span data-ttu-id="d0fd6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0fd6-114">-DefaultProfile</span></span>
<span data-ttu-id="d0fd6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0fd6-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="d0fd6-116">-ListKerbKey</span></span>
<span data-ttu-id="d0fd6-117">Zawiera listę kluczy Kerberos (jeśli włączono usługę Active Directory) dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="d0fd6-118">Klucz Kerberos jest generowany na konto magazynu na podstawie uwierzytelniania opartego na tożsamości plików Azure za pomocą usługi domeny Azure Active Directory (Azure AD DS) lub usługi domeny Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="d0fd6-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="d0fd6-119">Jest on używany jako hasło tożsamości zarejestrowanej w usłudze domeny, która reprezentuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="d0fd6-120">Klucz Kerberos nie zapewnia uprawnień dostępu do wykonywania jakichkolwiek operacji odczytu lub zapisu samolotów danych na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="d0fd6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0fd6-121">-Name</span></span>
<span data-ttu-id="d0fd6-122">Określa nazwę konta magazynu, dla którego to polecenie cmdlet otrzymuje klucze.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0fd6-124">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d0fd6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fd6-125">CommonParameters</span></span>
<span data-ttu-id="d0fd6-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0fd6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fd6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0fd6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fd6-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0fd6-128">INPUTS</span></span>

### <span data-ttu-id="d0fd6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d0fd6-129">System.String</span></span>

## <span data-ttu-id="d0fd6-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0fd6-130">OUTPUTS</span></span>

### <span data-ttu-id="d0fd6-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0fd6-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="d0fd6-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0fd6-132">NOTES</span></span>

## <span data-ttu-id="d0fd6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0fd6-133">RELATED LINKS</span></span>

[<span data-ttu-id="d0fd6-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0fd6-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


