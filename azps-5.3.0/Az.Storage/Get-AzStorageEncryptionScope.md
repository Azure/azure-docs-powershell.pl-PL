---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498198"
---
# <span data-ttu-id="ea33d-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ea33d-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="ea33d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea33d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea33d-103">Uzyskiwanie lub wyświetlanie listy zakresów szyfrowania z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea33d-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="ea33d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea33d-104">SYNTAX</span></span>

### <span data-ttu-id="ea33d-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ea33d-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea33d-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="ea33d-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea33d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea33d-107">DESCRIPTION</span></span>
<span data-ttu-id="ea33d-108">Polecenie cmdlet **Get-AzStorageEncryptionScope** Pobiera lub wyświetla zakresy szyfrowania z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea33d-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="ea33d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea33d-109">EXAMPLES</span></span>

### <span data-ttu-id="ea33d-110">Przykład 1: uzyskiwanie pojedynczego zakresu szyfrowania</span><span class="sxs-lookup"><span data-stu-id="ea33d-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="ea33d-111">To polecenie pobiera jeden zakres szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ea33d-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="ea33d-112">Przykład 2: wyświetlanie wszystkich zakresów szyfrowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ea33d-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="ea33d-113">To polecenie wyświetla listę wszystkich zakresów szyfrowania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea33d-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="ea33d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea33d-114">PARAMETERS</span></span>

### <span data-ttu-id="ea33d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea33d-115">-DefaultProfile</span></span>
<span data-ttu-id="ea33d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea33d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea33d-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="ea33d-117">-EncryptionScopeName</span></span>
<span data-ttu-id="ea33d-118">Nazwa usługi Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ea33d-118">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="ea33d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea33d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea33d-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea33d-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea33d-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea33d-121">-StorageAccount</span></span>
<span data-ttu-id="ea33d-122">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ea33d-122">Storage account object</span></span>

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

### <span data-ttu-id="ea33d-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea33d-123">-StorageAccountName</span></span>
<span data-ttu-id="ea33d-124">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea33d-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="ea33d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea33d-125">CommonParameters</span></span>
<span data-ttu-id="ea33d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea33d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea33d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea33d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea33d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea33d-128">INPUTS</span></span>

### <span data-ttu-id="ea33d-129">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea33d-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ea33d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea33d-130">OUTPUTS</span></span>

### <span data-ttu-id="ea33d-131">Microsoft. Azure. Commands. Management. Storage. models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ea33d-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="ea33d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea33d-132">NOTES</span></span>

## <span data-ttu-id="ea33d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea33d-133">RELATED LINKS</span></span>
