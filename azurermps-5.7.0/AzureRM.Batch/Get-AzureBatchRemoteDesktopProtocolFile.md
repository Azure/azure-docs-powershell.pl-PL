---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527101"
---
# <span data-ttu-id="9195f-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="9195f-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="9195f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9195f-102">SYNOPSIS</span></span>
<span data-ttu-id="9195f-103">Pobiera plik RDP z węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="9195f-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9195f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9195f-104">SYNTAX</span></span>

### <span data-ttu-id="9195f-105">Id_Path (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9195f-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9195f-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="9195f-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9195f-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="9195f-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9195f-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="9195f-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9195f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9195f-109">DESCRIPTION</span></span>
<span data-ttu-id="9195f-110">Polecenie cmdlet **Get-AzureBatchRemoteDesktopProtocolFile** pobiera plik RDP (Remote Desktop Protocol) z węzła compute i zapisuje go jako plik lub w strumieniu dostarczonym przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9195f-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="9195f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9195f-111">EXAMPLES</span></span>

### <span data-ttu-id="9195f-112">Przykład 1: pobranie pliku RDP z określonego węzła obliczeniowego i zapisanie pliku</span><span class="sxs-lookup"><span data-stu-id="9195f-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="9195f-113">To polecenie pobiera plik RDP z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="9195f-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9195f-114">Polecenie zapisuje plik RDP jako C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="9195f-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="9195f-115">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9195f-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9195f-116">Przykład 2: uzyskiwanie pliku RDP z węzła compute i zapisywanie pliku przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="9195f-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="9195f-117">To polecenie uzyskuje węzeł obliczeniowy z IDENTYFIKATORem ComputeNode02 w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="9195f-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9195f-118">Polecenie przekazuje ten węzeł obliczeniowy do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9195f-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9195f-119">Bieżące polecenie cmdlet pobiera plik RPD z węzła compute, a następnie zapisuje zawartość jako plik o nazwie C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="9195f-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="9195f-120">Przykład 3: uzyskiwanie pliku RDP z określonego węzła obliczeniowego i kierowanie go do strumienia</span><span class="sxs-lookup"><span data-stu-id="9195f-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="9195f-121">Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.</span><span class="sxs-lookup"><span data-stu-id="9195f-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="9195f-122">Drugie polecenie pobiera plik RDP z węzła obliczeniowego o IDENTYFIKATORze ComputeNode03 w puli o IDENTYFIKATORze Pool06.</span><span class="sxs-lookup"><span data-stu-id="9195f-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9195f-123">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="9195f-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="9195f-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9195f-124">PARAMETERS</span></span>

### <span data-ttu-id="9195f-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9195f-125">-BatchContext</span></span>
<span data-ttu-id="9195f-126">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9195f-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9195f-127">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9195f-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9195f-128">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9195f-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9195f-129">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="9195f-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9195f-130">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9195f-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9195f-131">-ComputeNode</span></span>
<span data-ttu-id="9195f-132">Określa węzeł obliczeniowy jako obiekt **PSComputeNode** , na który wskazuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="9195f-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="9195f-133">Aby uzyskać obiekt węzła obliczeniowego, użyj polecenia cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="9195f-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9195f-134">-ComputeNodeId</span></span>
<span data-ttu-id="9195f-135">Określa identyfikator węzła obliczeniowego, na którym znajduje się plik RDP.</span><span class="sxs-lookup"><span data-stu-id="9195f-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9195f-136">-DefaultProfile</span></span>
<span data-ttu-id="9195f-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9195f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="9195f-138">-DestinationPath</span></span>
<span data-ttu-id="9195f-139">Określa ścieżkę pliku, w którym to polecenie cmdlet zapisuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="9195f-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="9195f-140">-DestinationStream</span></span>
<span data-ttu-id="9195f-141">Określa strumień, do którego to polecenie cmdlet kieruje dane RDP.</span><span class="sxs-lookup"><span data-stu-id="9195f-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="9195f-142">To polecenie cmdlet nie zamyka ani nie Przewija tego strumienia.</span><span class="sxs-lookup"><span data-stu-id="9195f-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9195f-143">-PoolId</span></span>
<span data-ttu-id="9195f-144">Określa identyfikator puli zawierającej węzeł obliczeniowy, na podstawie którego to polecenie cmdlet pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="9195f-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9195f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9195f-145">CommonParameters</span></span>
<span data-ttu-id="9195f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9195f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9195f-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9195f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9195f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9195f-148">INPUTS</span></span>

### <span data-ttu-id="9195f-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9195f-149">BatchAccountContext</span></span>
<span data-ttu-id="9195f-150">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9195f-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9195f-151">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9195f-151">PSComputeNode</span></span>
<span data-ttu-id="9195f-152">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9195f-152">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="9195f-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9195f-153">OUTPUTS</span></span>

## <span data-ttu-id="9195f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9195f-154">NOTES</span></span>

## <span data-ttu-id="9195f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9195f-155">RELATED LINKS</span></span>

[<span data-ttu-id="9195f-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9195f-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9195f-157">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9195f-157">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="9195f-158">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="9195f-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


