---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178202"
---
# <span data-ttu-id="e75e1-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e75e1-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="e75e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e75e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e75e1-103">Pobierz lub z listy zakresów szyfrowania z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e75e1-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="e75e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e75e1-104">SYNTAX</span></span>

### <span data-ttu-id="e75e1-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="e75e1-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e75e1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e75e1-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e75e1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e75e1-107">DESCRIPTION</span></span>
<span data-ttu-id="e75e1-108">Polecenie **cmdlet Get-AzStorageEncryptionScope** pobiera lub wyświetla zakresy szyfrowania z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e75e1-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="e75e1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e75e1-109">EXAMPLES</span></span>

### <span data-ttu-id="e75e1-110">Przykład 1. Uzyskiwanie pojedynczego zakresu szyfrowania</span><span class="sxs-lookup"><span data-stu-id="e75e1-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="e75e1-111">To polecenie ma pojedynczy zakres szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="e75e1-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="e75e1-112">Przykład 2. Lista wszystkich zakresów szyfrowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e75e1-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="e75e1-113">To polecenie zawiera listę wszystkich zakresów szyfrowania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e75e1-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="e75e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e75e1-114">PARAMETERS</span></span>

### <span data-ttu-id="e75e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75e1-115">-DefaultProfile</span></span>
<span data-ttu-id="e75e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e75e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e75e1-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="e75e1-117">-EncryptionScopeName</span></span>
<span data-ttu-id="e75e1-118">Nazwa szyfrowania magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e75e1-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e75e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="e75e1-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e75e1-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e75e1-121">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e75e1-121">-StorageAccount</span></span>
<span data-ttu-id="e75e1-122">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e75e1-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e75e1-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e75e1-123">-StorageAccountName</span></span>
<span data-ttu-id="e75e1-124">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e75e1-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e75e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75e1-125">CommonParameters</span></span>
<span data-ttu-id="e75e1-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e75e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75e1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e75e1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75e1-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e75e1-128">INPUTS</span></span>

### <span data-ttu-id="e75e1-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e75e1-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e75e1-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e75e1-130">OUTPUTS</span></span>

### <span data-ttu-id="e75e1-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e75e1-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="e75e1-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e75e1-132">NOTES</span></span>

## <span data-ttu-id="e75e1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e75e1-133">RELATED LINKS</span></span>
